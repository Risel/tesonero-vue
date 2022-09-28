<template>
  <header>
    <Header/>
  </header>
  <main class="main__wrapper">
    <div class="green-line">
    </div>
    <h1 class="main__wrapper-title">Lorem ipsum, dolor sit amet consectetur</h1>
    <CarouselDesktop/>
  </main>
</template>

<script>

import Header from '@/components/Header.vue';
import CarouselDesktop from '@/components/Carousel.vue';

export default {
  name: 'App',
  components: {
    CarouselDesktop,
    Header,
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

.main__wrapper{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 75px 0;
  background: linear-gradient(111.04deg, #E2E2E2 0.39%, rgba(255, 255, 255, 0) 86.46%);
  &-title{
    color: $blue;
    text-transform: uppercase;
    font-size: 40px;
    font-weight: 700;
  }
}
.green-line {
  width: 11rem;
  height: 4px;
  background-color:$green;
  margin-bottom: 22px;
}
</style>
