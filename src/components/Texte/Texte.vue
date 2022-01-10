<template>
  <div :class="titleClass">
    {{ text }}
  </div>
</template>

<script>
export default {
  props: {
    text: { type: String, default: "" },
    titleClass: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="css" scoped>
.title {
  text-align: center;
  font-size: 42px;
  text-transform: capitalize;
  margin-bottom: 1.75rem;
}
.text {
  font-size: 24px;
  text-align: center;
  white-space: pre-wrap;
  font-family: "Graphik", sans-serif;
  font-weight: lighter;
  font-style: normal;
  margin-bottom: 2.5rem;
}
</style>