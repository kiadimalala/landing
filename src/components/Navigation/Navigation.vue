<template>
  <div class="navigation">
    <div class="nav">
      <ul class="nav_links">
        <li class="nav_items" v-for="(link, index) in links" :key="index">
          <a href="#"> {{ link }} </a>
        </li>
      </ul>
      <span class="logo">
        <svg-base>
          <logo></logo>
        </svg-base>
      </span>
    </div>
    <div class="right">
      <svg-base svg-class="social_icon">
        <twitter></twitter>
      </svg-base>
      <svg-base svg-class="social_icon">
        <facebook></facebook>
      </svg-base>
      <svg-base svg-class="social_icon">
        <linkedin></linkedin>
      </svg-base>
      <svg-base svg-class="social_icon menu">
        <Menu />
      </svg-base>
    </div>
  </div>
</template>

<script>
import Logo from "../SVG/Logo.vue";
import SvgBase from "../SVG/SvgBase.vue";
import Twitter from "../SVG/Twitter.vue";
import Facebook from "../SVG/Facebook.vue";
import Linkedin from "../SVG/Linkedin.vue";
import Menu from "../SVG/Menu.vue";
export default {
  components: { SvgBase, Logo, Twitter, Facebook, Linkedin, Menu },
  data() {
    return {
      links: ["home", "product", "pricing", "about", "contact"],
      socials: [
        {
          name: "twitter",
          components: "<twitter></twitter>",
        },
        {
          name: "facebook",
          components: "<facebook></facebook>",
        },
        {
          name: "linkedin",
          components: "<linkedin></linkedin>",
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped>
.navigation {
  height: 10%;
  margin: 3.75rem 0;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding: 0 2.25rem;
}
.nav {
  width: 70%;
  height: 100%;
  display: flex;
  align-items: center;
}
.right {
  width: 30%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  height: 58px;
}
.nav .nav_links {
  width: 60%;
  height: 58px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.nav .logo {
  width: 45%;
}

.nav_links .nav_items {
  list-style: none;
}

.nav_links .nav_items a {
  text-transform: capitalize;
  text-decoration: none;
  color: var(--light-text);
}
@media (max-width: 426px) {
  .navigation {
    padding: 0;
  }
  .nav .nav_links {
    display: none;
  }
}

</style>