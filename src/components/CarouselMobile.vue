<template>
    <div class="carousel__header">
      <img src="@/assets/berries.png" alt="berries">
      <h1 class="carousel__header-title">Lorem ipsum, dolor sit amet consectetur</h1>
    </div>
    <Carousel ref="carousel" class="carousel">
      <Slide v-for="element in elements" :key="element">
        <div class="carousel__item">
          <img :src="element.icon" alt="icon">
          <p>{{element.description}}</p>
        </div>
      </Slide>
    </Carousel>
    <div class="carousel__navigation">
      <img src="@/assets/arrow_left.svg" alt="prev" @click="prev">
      <div v-for="element in elements" :key="element.id" class="carousel__navigation-dots">
        <svg width="8" height="8" viewBox="0 0 8 8"
             fill="none" xmlns="http://www.w3.org/2000/svg"
        >
          <rect width="8" height="8" rx="4"
                fill="#E7EBF0"
                :class="element.id === activeId ? 'carousel__navigation-dots_dot' : '' "
          />
        </svg>
      </div>
      <img src="@/assets/arrow_right.svg" alt="next" @click="next">
    </div>
</template>

<script>
import {
  Carousel, Slide,
} from 'vue3-carousel';
import headset from '@/assets/headset.svg';
import box from '@/assets/box.svg';
import label from '@/assets/label.svg';
import tablet from '@/assets/tablet.svg';

import 'vue3-carousel/dist/carousel.css';

export default {
  name: 'carousel-mobile',
  components: {
    Carousel,
    Slide,
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
      activeId: 1,
    };
  },
  methods: {
    next() {
      this.$refs.carousel.next();
      if (this.activeId < 6) {
        this.activeId += 1;
      }
    },
    prev() {
      this.$refs.carousel.prev();
      if (this.activeId > 1) {
        this.activeId -= 1;
      }
    },
  },
};

</script>

<style lang="scss" scoped>
.carousel {
  &__header {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    img {
      position: absolute;
      width: 100%;
      top: -4rem;
      @media screen and (min-width: 460px) {
        top: -6.75rem;
      }
    }
    &-title{
      margin-top: 8rem;
      color: $blue;
      text-transform: uppercase;
      font-size: 24px;
      font-weight: 700;
      text-align: center;
    }
  }

  &__item{
    margin: 1rem auto;
    width: 50%;
    color: $blue;
    font-size: 16px;
  }
  &__navigation {
    display: flex;
    flex-direction: row;
    &-dots {
      padding: 0.5rem;
      &_dot{
        fill: #A6ABBD;
      }
    }
  }
}
</style>
