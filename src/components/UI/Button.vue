<template>
  <button class="button" :class="{ 'button_active' : isActive }">
        <span class="button__text">
            <slot></slot>
        </span>
  </button>
</template>

<script>
export default {
  name: 'MyButton',
  props: {
    isActive: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.button {
  border: 0;
  background-color: transparent;
  color: $gray;
  padding: 0.25rem 1.5rem;
  border-radius: 0.5rem;

  &:hover {
    cursor: pointer;
  }

  &_active {
    &:hover {
      background-color: $green;
    }

    background-color: $green;
    color: #fff;
    box-shadow: $box-shadow;

  }

  &__text {
    line-height: 1.5rem;
  }
}
</style>
