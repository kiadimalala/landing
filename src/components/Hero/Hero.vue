<template>
  <div class="hero">
    <h1>The best product start with figma</h1>
    <h4>
      Most calendars are designed for teams. Slate is designed for freelancers
    </h4>
    <Button btn-class="btn_big" label="try for free"></Button>
  </div>
</template>

<script>
import Button from "../Button/Button.vue";
export default {
  components: { Button },
};
</script>

<style lang="css" scoped>
.hero {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: var(--light-text);
}
.hero h1 {
  font-size: 4rem;
  text-align: center;
  font-family: "Graphik", sans-serif;
  font-weight: 900;
  font-style: normal;
  line-height: 1.2;
  margin: 2rem 14rem;
  letter-spacing: 0.2px;
}
.hero h4 {
  font-size: 1.65rem;
  margin: 0 14rem;
  text-align: center;
  font-weight: normal;
}
</style>