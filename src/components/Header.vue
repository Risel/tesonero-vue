<template>
    <nav class="nav">
      <div class="nav__items">
        <img src="@/assets/logo.svg" alt="logo" class="nav__logo">
        <MyButton class="nav__items-item">
          NavItem1
        </MyButton>
        <MyButton class="nav__items-item">
          NavItem2
        </MyButton>
        <MyButton isActive="true" class="nav__items-item">
          NavItem3
        </MyButton>
      </div>
      <div class = "nav-end">
        <MyButton isActive = "true" class="nav__items-item">
          Button
        </MyButton>
      </div>
    </nav>
</template>

<script>
import MyButton from '@/components/UI/Button.vue';

export default {
  name: 'MainHeader',
  components: {
    MyButton,
  },

};
</script>

<style lang="scss" scoped>
.nav{
  width: 100%;
  height: 160px;
  background-color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__items{
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin-left: 87px;

    &-item {
      margin-left: 87px;
    }
  }
  &-end {
    margin-right: 84px;
  }
}
</style>
