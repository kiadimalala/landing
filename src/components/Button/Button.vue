<template>
  <button :class="btnClass" v-on="$listenersbbb">
    {{ label }}
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: {
    btnClass: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="css" scoped>
.btn_big {
  width: 236px;
  height: 52px;
  border-radius: 35px;
  border: none;
  background-color: var(--primary);
  color: var(--light-text);
  font-size: 20px;
  text-transform: capitalize;
  margin: 4.75rem 0;
}
</style>