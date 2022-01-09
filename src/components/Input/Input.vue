<template>
  <div>
    <label v-if="label">
      {{ label }}
    </label>
    <input @input="updateValue" :value="value" v-bind="$attrs" />
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: {
    label: {
      type: String,
      default: "",
    },
    value: {
      type: [String, Number],
    },
  },
  methods: {
    updateValue(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>

<style lang="scss" scoped>
/* clip-path: polygon(0 0, 100% 0%, 100% 50%, 49% 99%, 0% 50%); */
</style>