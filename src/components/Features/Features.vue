<template>
  <Section section-class="features">
    <div slot="content">
      <Texte title-class="title" text="features" />
      <Texte
        title-class="text"
        text="Most calendars are designed for teams. 
Slate is designed for freelancers"
      />
      <div class="card_container">
        <div :v-html="T"></div>
      </div>
    </div>
  </Section>
</template>

<script>
import Section from "../Section/Section.vue";
import Texte from "../Texte/Texte.vue";
export default {
  data() {
    return {
      T: `<Texte text="demo/>`,
    };
  },
  components: {
    Section,
    Texte,
  },
};
</script>

<style lang="postcss" scoped>
.card_container {
  width: 869px;
  height: 257px;
  margin: auto;
}
</style>