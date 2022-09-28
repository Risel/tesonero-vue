<template>
  <img src="@/assets/berries.png" alt="berries" class="berries">
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

export default {
  name: 'carousel-desktop',
  components: { CarouselCard },
  data() {
    return {
      elements: [
        {
          id: 1,
          icon: headset,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 2,
          icon: box,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 3,
          icon: label,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 4,
          icon: box,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 5,
          icon: headset,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },
        {
          id: 6,
          icon: tablet,
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit.',
        },

      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.berries {
  position: absolute;
  top: 530px;
}
.carousel {
  animation: spin 3s infinite;
  position: relative;
  width: 37rem;
  height: 37rem;
  border-radius: 50%;
  padding: 0;
  list-style: none;
  margin: 7rem auto;
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
@keyframes spin {
  from {
    transform:rotate(0deg);
  }
  to {
    transform:rotate(360deg);
  }
}
</style>
