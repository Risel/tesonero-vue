<template>
  <div class="card">
    <img :src="icon" alt="icon" class="card__icon">
    <p class="card__text">{{description}}</p>
  </div>

</template>

<script>
export default {
  name: 'carousel-card',
  props: {
    icon: String,
    description: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  align-items: center;
  width: 14rem;
  &__icon {
    width: 6.25rem;
    height: 6.25rem;
  }
  &__text {
    text-align: center;
  }
}
</style>
