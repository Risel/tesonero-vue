<template>
  <div class="carousel__header">
    <green-divider/>
    <h1 class="carousel__header-title">Lorem ipsum, dolor sit amet consectetur</h1>
  </div>
  <img
    src="@/assets/bubbles-2.svg"
    alt="bubbles"
    class="carousel__background-bubbles carousel__background-bubbles_left"
  >
  <img
    src="@/assets/bubbles-1.svg"
    alt="bubbles"
    class="carousel__background-bubbles carousel__background-bubbles_right"
  >
  <img
    src="@/assets/berries.png"
    alt="berries"
    class="background-mid"
  >
  <ul class="carousel">
    <carousel-card
      v-for="item in elements"
      :key="item.id"
      :icon="item.icon"
      :description="item.description"
    />
  </ul>
</template>

<script>
import headset from '@/assets/headset.svg';
import box from '@/assets/box.svg';
import label from '@/assets/label.svg';
import tablet from '@/assets/tablet.svg';
import CarouselCard from '@/components/CarouselCard.vue';
import GreenDivider from '@/components/UI/GreenDivider.vue';

export default {
  name: 'carousel-desktop',
  components: {
    CarouselCard,
    GreenDivider,
  },
  data() {
    return {
      elements: [
        {
          id: 1,
          icon: box,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 2,
          icon: headset,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 3,
          icon: tablet,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 4,
          icon: headset,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 5,
          icon: box,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 6,
          icon: label,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>

.carousel {
  position: relative;
  width: 37rem;
  height: 37rem;
  border-radius: 50%;
  padding: 0;
  list-style: none;
  margin: 7rem auto;
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
  img {
    width: 10rem;
    height: 10rem;
    border-radius: 50%;
    border: solid 5px #001529;
    display: block;
    max-width: 100%;
    max-height: 100%;
    transition: 0.15s;
  }

  & > * {
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    margin: -7rem;
    text-align: center;
    width: 12rem;
    height: 16rem;
  }

  & > *:nth-of-type(0) {
    transform: rotate(0deg) translate(20rem) rotate(0deg);
  }

  & > *:nth-of-type(1) {
    transform: rotate(60deg) translate(20rem) rotate(-60deg);
  }

  & > *:nth-of-type(2) {
    transform: rotate(120deg) translate(20rem) rotate(-120deg);
  }

  & > *:nth-of-type(3) {
    transform: rotate(180deg) translate(20rem) rotate(-180deg);
  }

  & > *:nth-of-type(4) {
    transform: rotate(240deg) translate(20rem) rotate(-240deg);
  }

  & > *:nth-of-type(5) {
    transform: rotate(300deg) translate(20rem) rotate(-300deg);
  }

  & > *:nth-of-type(6) {
    transform: rotate(360deg) translate(20rem) rotate(-360deg);
  }
}

.background-mid {
  position: absolute;
  filter: drop-shadow(0px 40px 80px rgba(0, 0, 0, 0.16));
  top: 25.5rem;
  width: 37rem;
}

.carousel__item {
  min-height: 200px;
  width: 100%;
  color: $blue;
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
