<template>
  <nav class="navbar" :class="{ 'blur-bg': navIsOpen === true }">
    <div class="container-lg">

      <div>
        <router-link class="navbar-brand logo green" href="#">
          <img src="../assets/images/logo.svg" class-="logo" alt="logo">
        </router-link>
      </div>

      <div class="navi-items">
        <button class="navbar-toggle" type="button" aria-label="Toggle navigation" 
        :class="{ 'aside-color': navIsOpen }"
        @click="toggleNav">
          <span class="toggler-icon top-bar"
          :class="{ 'top-icon-animate': navIsOpen }"></span>
          <span class="toggler-icon middle-bar"
          :class="{ 'middle-icon-animate': navIsOpen }"></span>
          <span class="toggler-icon bottom-bar"
          :class="{ 'bottom-icon-animate': navIsOpen }"></span>
        </button>
        <ul class= "navbar-navi">
          <li class="navbar-item">
            <router-link class="navbar-link" href="#">Individual</router-link>
          </li>
          <li class="navbar-item">
            <router-link class="navbar-link" href="#">Business</router-link>
          </li>
          <li class="navbar-item">
            <router-link class="navbar-link" href="#">Pricing</router-link>
          </li>
          <li class="navbar-item">
            <router-link class="navbar-link" href="#">Set your payroll</router-link>
          </li>
        </ul>
      </div>
      
      <div class="buttons d-flex">
        <li class="navbar-item">
          <button class="btn btn1">Log in</button>
        </li>
        <li class="navbar-item">
          <button class="btn btn2">Register</button>
        </li>
      </div>
    </div>
  </nav>

  <!-- mobile navigation  -->
  <div
    class="backdrop"
    @wheel.prevent
    @touchmove.prevent
    @scroll.prevent
    @touch.self="toggleNav"
    @click.self="toggleNav"
    v-show="navIsOpen"
  >
    <aside :class="{ 'leave-animation': !navIsOpen, 'invisible': clicked === 0, }">
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">Individual</router-link>
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">Business</router-link>
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">Pricing</router-link>
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">Set your payroll</router-link>
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">
        <button class="btn btn1 mobile-btn">Log in</button>
      </router-link>
      <router-link class="navbar-link block light-slate" href="#" @click="toggleNav">
        <button class="btn btn2">Register</button>
      </router-link>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      clicked: 0,
    }
  },
  props: {
    navIsOpen: Boolean,
  },
  emits: ['toggle-nav'],
  methods: {
    toggleNav() {
      this.$emit('toggle-nav');
      this.clicked = 1
    },
  },
  computed: {
    canOpenNav() {
      return (this.navIsOpen === false && this.clicked === 1)
    }
  }
}
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  text-decoration: none;
  list-style: none;
  box-sizing: border-box;
  position: relative;
}
nav {
  background-color: #FFF;
  color: #515251;
  display: flex;
  justify-content: space-between;
  position: relative;
  width: 100%;
  padding: 1rem 0;
}
div.backdrop {
    position: fixed;
    overflow: hidden;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    backdrop-filter: blur(5px);
    transition: display 0.5s;
    z-index: 10;
}
aside {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  position: fixed;
  width: min(75vw, 400px);
  height: 100vh;
  right: 0;
  top: 0;
  background-color: #FFF;
  color: #11453B;
  text-align: center;
  transform: translateX(1000px);
  z-index: 10;
  padding: 80px 10px;
  transition: transform 0.5s linear;
  animation: show 0.5s linear forwards;
}
.aside-color {
    background-color: #FFF !important;
    position: absolute;

}
aside button.btn {
    background-color: #FFF;
    font-size: 17px;
    padding: 3% 10% !important;
}
@keyframes show {
  from {
    transform: translateX(1000px);
  }
  to {
   transform: translateX(0px);
  }
}
.leave-animation {
  animation: leave 0.5s linear backwards !important;
}
@keyframes leave {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(1000px);
  }
}
.invisible {
  opacity: 0;
}
.show {
  animation: show 0.5s linear forwards;
}
.navbar-brand img {
  width: 7rem;
  z-index: 1000;
}
@keyframes flip {
  from {
    transform: rotateY(0deg);
  }
  to {
    transform: rotateY(360deg);
  }
}
li {
  font-size: 0.8rem;
  padding: 10px;
  text-decoration: none;
}
li.navbar-item {
  display: flex;
  align-items: center;
  padding-left: 1rem;
}
button.navbar-toggle {
  background-color: #FFF;
  border-style: none;
  display: none;
  position: relative;
  cursor: pointer;
  width: 30px;
  height: 30px;
  z-index: 1000;
}
span.top-bar {
  margin-top: -10px;
  transform: rotate(0deg);
  border-radius: 32px;
}
span.middle-bar {
  opacity: 1;
  filter: alpha(opacity=100);
  border-radius: 32px;
}
span.bottom-bar {
  margin-top: 10px;
  transform: rotate(0deg);
  border-radius: 32px;
}
.navbar-link {
  color: #515251;
  font-size: 1rem;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}
.navbar-link:hover {
  color: #11453B;
}
.toggler-icon {
  display: block;
  display: none;
  position: absolute;
  height: 2px;
  width: 100%;
  background: #11453B;
  opacity: 1;
  left: 0;
  transform: rotate(0deg);
  transition: .25s ease-in-out;
}
.navi-items {
  display: flex;
}
.navbar-navi {
  display: flex;
  justify-content: space-between;
}
.top-icon-animate {
  margin-top: 0px !important;
  transform: rotate(135deg) !important;
}
.middle-icon-animate {
  opacity: 0 !important;
  filter: alpha(opacity=0) !important;
}
.bottom-icon-animate {
  margin-top: 0px !important;
  transform: rotate(-135deg) !important;
  width: 100% !important;
}
.block {
  display: block;
  font-size: 17px;
  padding-top: 0;
  transform: translateY(-22px);
}
button.btn {
  font-size: 1rem;
  padding: 0.3rem 2rem;
  border-radius: 24px;
  transition: all 0.5s linear;
  box-shadow: 0px 8px 16px 0px rgba(17, 69, 59, 0.20);
}
/* .btn1:nth-of-type(1) {
  margin-left: 3rem;
} */
.btn1 {
  background-color: #FFF;
  border: #11453B 1px solid;
  color: #11453B;
}
.btn.mobile-btn {
  margin-left: 0;
}
.btn2 {
  background-color: #11453B !important;
  border: #11453B 1px solid;
  color: #FFF;
}
@media (min-width: 769px) {
    aside {
        display: none;
    }
}
@media (max-width: 992px) {
  /* .navi-items {
    left: 8rem;
  } */
  .btn1:nth-of-type(1) {
    margin-left: 1rem;
  }
}
@media (min-width: 820px) {
  .blur-bg {
    backdrop-filter: blur(3px);
    /* background-color: rgba(10, 25, 47, 0.1); */
  }
}
@media (max-width: 868px) {
  .navbar-brand img {
    width: 7rem;
  }
  ul.navbar-navi {
    display: none;
  }
  div.buttons {
    display: none !important;
  }
  button.navbar-toggle {
    display: block;
    margin-right: 10px;
    z-index: 11;
    width: 1.5rem;
    height: 1.5rem;
  }
  .toggler-icon {
    display: block;
  }
  /* .blur-bg {
    backdrop-filter: none;
    background-color: rgba(10, 25, 47, 1);
  } */
}
@media (max-height: 700px) {
  aside {
    padding: 80px 10px 25px;
  }
  aside .navbar-link {
    padding-top: 20px;
  }
}
</style>
