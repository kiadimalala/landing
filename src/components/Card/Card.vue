<template>
  <div :class="cardClass">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    cardClass: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss" scoped>
</style>