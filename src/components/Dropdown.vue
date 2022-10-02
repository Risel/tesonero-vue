<template>
  <div class = "dropdown">
    <div class="dropdown__header" @click="$emit('toggle-dropdown',id)">
      <img class="dropdown__header-icon" :src="icon" alt="icon">
      <h3 class="dropdown__header-title"
          :class="{'dropdown__header-title_active': isActive}"
      >
        {{title}}
      </h3>
      <img class="dropdown__header-arrow" src="@/assets/arrow_down.svg" alt="arrow"
           :class="{'dropdown__header-arrow_flip':isActive}"
      >
    </div>
    <div :class="{'dropdown__text': !isActive}">
      <div class="dropdown__text-body"><p>{{body}}</p></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'faq-dropdown',
  props: {
    id: Number,
    icon: String,
    title: String,
    body: String,
    isActive: Boolean,
  },
};
</script>

<style lang="scss" scoped>
.dropdown {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-bottom: 1px solid #E7EBF0;
  color: $blue;

  &__header {
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    &-icon {
      width: 2.5rem;
      height: 2.5rem;
      margin-right: 1.5rem;
    }
    &-title {
      font-size: 24px;
      font-weight: 700;
      transition: all 0.2s ease-in;

      &_active {
        color: $green;
      }
    }
    &-arrow {
      margin-left: auto;
      transition: all 0.25s ease ;
      &_flip {
        transform: rotate(180deg);
      }
    }
  }
  &__text {
    display: none;
  }
}
</style>
