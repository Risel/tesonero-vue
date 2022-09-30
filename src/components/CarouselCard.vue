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
  color:$blue;
  font-size: 16px;

  &__icon {
    width: 7rem;
    height: 7rem;
  }
  &__text {
    text-align: center;
  }
}
</style>
