<template>
  <div :class="svgClass">
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    svgClass: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="css" scoped>
.social_icon {
  font-size: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--light-text);
  margin: 0 1rem;
}
.menu {
  display: none;
}

@media (max-width: 426px) {
  .social_icon {
    display: none;
  }
  .menu {
    display: flex;
  }
}
</style>