<template>
  <header>
    <Header/>
  </header>
  <main class="main">
    <img
      src="@/assets/bubbles-2.svg"
      alt="bubbles"
      class="main__background-bubbles main__background-bubbles_left"
    >
    <img
      src="@/assets/bubbles-1.svg"
      alt="bubbles"
      class="main__background-bubbles main__background-bubbles_right"
    >
    <div class="main__header">
      <green-devider/>
      <h1 class="main__header-title">Lorem ipsum, dolor sit amet consectetur</h1>
    </div>
    <CarouselDesktop class="main__items"/>
  </main>
  <footer>
    <div class="footer__wrapper">
      <Testimonials/>
      <FAQ/>
    </div>
  </footer>
</template>

<script>

import Header from '@/components/Header.vue';
import CarouselDesktop from '@/components/Carousel.vue';
import GreenDevider from '@/components/UI/GreenDevider.vue';
import Testimonials from '@/components/Testimonials.vue';
import FAQ from '@/components/FAQ.vue';

export default {
  name: 'App',
  components: {
    Testimonials,
    CarouselDesktop,
    GreenDevider,
    Header,
    FAQ,
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

.main{
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 75px 0;
  background: linear-gradient(111.04deg, #E2E2E2 0.39%, rgba(255, 255, 255, 0) 86.46%);
  width: 100%;
  overflow: hidden;
  &__header {
    display: flex;
    flex-direction: column;
    align-items: center;

    &-title{
      color: $blue;
      text-transform: uppercase;
      font-size: 40px;
      font-weight: 700;
    }
  }

  &__background-bubbles {
    position: absolute;
    filter:blur(5px);
    &_left{
      left: 0;
      bottom: -5rem;
      width: 27.5rem;
      transform:rotate(55.73deg)
    }
    &_right{
      top: 5rem;
      right: -4rem;
      width: 36.75rem;
      transform:rotate(135.54deg);
    }
  }
}

.footer__wrapper{
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-shrink: 0;
  position: relative;
  flex-grow: 0;
}
</style>
