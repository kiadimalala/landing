<template>
  <div id="app">
    <Layout>
      <Section section-class="header">
        <img
          class="img"
          src="./assets/images/background.png"
          alt=""
          slot="background"
        />
        <div class="content" slot="content">
          <Navigation />
          <Hero />
        </div>
      </Section>
      
    </Layout>
  </div>
</template>

<script>
import Layout from "./Layout/Layout.vue";
import Section from "./components/Section/Section";
import Navigation from "./components/Navigation/Navigation.vue";
import Hero from "./components/Hero/Hero.vue";
export default {
  name: "App",
  components: { Layout, Section, Navigation, Hero },
};
</script>

<style>
#app {
  color: #2c3e50;
  height: 100%;
  font-family: "Graphik", sans-serif;
}
body,
html {
  margin: 0;
  padding: 0;
  height: 100%;
  font-size: 16px;
}
</style>
