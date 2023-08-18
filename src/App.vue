<template>
    <div>

      <!-- Navigation bar  -->
      <div class="nav-container container-lg">
        <NavBar :navIsOpen="navIsOpen"
          @toggle-nav="navIsOpen = !navIsOpen"
        >
        </NavBar>
      </div>

      <img src="./assets/images/blob.png" class="blob blob1" alt="blob">
      <img src="./assets/images/blob.png" class="blob blob2" alt="blob">
      <img src="./assets/images/blob.png" class="blob blob3" alt="blob">

      <!-- Hero section -->
      <div class="mt-5">
        <HeroSection></HeroSection>
      </div>

      <div>
        <FeatureSection></FeatureSection>
      </div>

      <div class="mt-5">
        <HowItWorks></HowItWorks>
      </div>

      <div class="subscribe">
        <Subscribe></Subscribe>
      </div>

      <div class="">
        <CallToAction></CallToAction>
      </div>

      <div>
        <FootingSection></FootingSection>
      </div>

    </div>
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import NavBar from './components/NavBar.vue'
import FeatureSection from './components/FeatureSection.vue'
import HowItWorks from './components/HowItWorks.vue'
import Subscribe from './components/Subscribe.vue';
import FootingSection from './components/FootingSection.vue';
import CallToAction from './components/CallToAction.vue';

export default {
  name: 'App',
  data() {
    return {
      navIsOpen: false,
      sticky: true,
      shouldFadeOut: false,
    }
  },
  mounted() {
    window.addEventListener('scroll', () => {
      let st = window.scrollY;
      if (st > 150) {
          this.shouldFadeOut = true
      } else {
          this.shouldFadeOut = false
      }
    });
  },
  components: {
    NavBar,
    HeroSection,
    FeatureSection,
    HowItWorks,
    Subscribe,
    FootingSection,
    CallToAction
}
}
</script>

<style scoped>
.blob1 {
  position: absolute;
  top: 0;
  width: 25rem;
}
.blob2 {
  position: absolute;
  right: 0rem;
  top: 0;
  width: 25rem;
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
}
.blob3 {
  position: absolute;
  width: 20rem;
  top: 25rem;
  left: 0;
  transform: rotate(270deg);
  z-index: -1;
}
@media (max-width: 768px) {
  .blob {
    width: 10rem;
    height: 15rem;
  }
  .blob1, .blob2 {
    top: 0;
  }
  .blob3 {
    top: 28rem;
  }
}
</style>
