<template>
  <div :class="['section', sectionClass]">
    <slot name="background" />
    <div class="container">
      <slot name="content" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    sectionClass: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="css" scoped>
.section {
  width: 100%;
  margin: auto;
}
.section .container {
  width: 75%;
  height: 100%;
  margin: auto;
}
.header {
  position: relative;
  height: 105%;
  width: 100%;
  clip-path: polygon(0 0, 100% 0%, 100% 75%, 50% 100%, 0% 75%);
}

.header .container {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  align-content: center;
  z-index: 1600;
}

.container .content {
  height: 80%;
}

.header .img {
  width: 100%;
  min-height: 100%;
  object-fit: cover;
  object-position: top;
}

@media (max-width: 426px) {
  .section .container {
    width: 90%;
  }
  .header {
    clip-path: polygon(0 0, 100% 0%, 100% 90%, 50% 100%, 0% 90%);
  }
}
</style>