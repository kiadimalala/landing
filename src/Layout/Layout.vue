<template>
  <div :class="['layout', layoutClass]">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    layoutClass: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="css" scoped>
.layout {
  width: 100%;
  height: 100%;
}
</style>