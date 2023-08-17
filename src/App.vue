<template>
    <div>

      <!-- Navigation bar  -->
      <div class="nav-container container-lg">
        <NavBar :navIsOpen="navIsOpen"
          @toggle-nav="navIsOpen = !navIsOpen"
        >
        </NavBar>
      </div>

      <img src="./assets/images/blob.png" class="blob1" alt="blob">
      <img src="./assets/images/blob.png" class="blob2" alt="blob">

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
    FootingSection
}
}
</script>

<style scoped>
.blob1 {
  position: absolute;
  width: 20rem;
}
.blob2 {
  position: absolute;
  right: 0rem;
  width: 20rem;
}
</style>
