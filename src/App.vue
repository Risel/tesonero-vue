<template>
  <header>
    <Header/>
  </header>
  <main class="main">
    <CarouselDesktop v-if="width > 950"/>
    <CarouselMobile v-else/>
  </main>
  <footer class="footer">
    <div class="footer__wrapper-desktop" v-if="width > 870">
      <Testimonials/>
      <FAQ/>
    </div>
    <div class="footer__wrapper-mobile" v-else>
      <FAQ/>
      <Testimonials/>
    </div>
  </footer>
</template>

<script>

import Header from '@/components/Header.vue';
import CarouselDesktop from '@/components/CarouselDesktop.vue';
import Testimonials from '@/components/Testimonials.vue';
import FAQ from '@/components/FAQ.vue';
import CarouselMobile from '@/components/CarouselMobile.vue';

export default {
  name: 'App',
  components: {
    CarouselMobile,
    Testimonials,
    CarouselDesktop,
    Header,
    FAQ,
  },
  data() {
    return {
      width: null,
    };
  },
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    },
  },
  created() {
    window.addEventListener('resize', this.updateWidth);
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Roboto,sans-serif;
}

.main {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
  padding: 75px 0;
  background: linear-gradient(111.04deg, #E2E2E2 0.39%, rgba(255, 255, 255, 0) 86.46%);
  width: 100%;
  overflow: hidden;
  @media screen and (max-width: 950px){
    background: #fff;
  }
}
.footer {
  &__wrapper-desktop {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-shrink: 0;
    position: relative;
    flex-grow: 0;
  }
  &__wrapper-mobile {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    position: relative;
  }
}
</style>
