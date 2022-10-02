<template>
  <div class="divider">
    <slot>
    </slot>
  </div>
</template>

<script>
export default {
  name: 'green-devider',
};
</script>

<style lang="scss" scoped>
.divider {
  width: 11rem;
  height: 4px;
  background-color:$green;
  margin-bottom: 1.375rem;
  @media screen and (max-width: 950px) {
    width: 65%;
  }
}
</style>
