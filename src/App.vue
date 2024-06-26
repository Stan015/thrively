<script setup>
import "./assets/main.css";
import { RouterLink, RouterView } from "vue-router";
import StarIcon from "./components/icons/IconStar.vue";
import DiscordIcon from "./components/icons/IconDiscord.vue";
import { Icon } from "@iconify/vue";

import { ref } from "vue";

const show = ref(false);
</script>

<template>
  <header>
    <a href="/"
      ><img
        alt="Vue logo"
        class="logo"
        src="/logo.svg"
        width="125"
        height="125"
    /></a>

    <nav :class="{'show-nav':show, 'hide-nav': !show}">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/">Books</RouterLink>
      <RouterLink to="/">Documentary</RouterLink>
      <RouterLink to="/">Careers</RouterLink>
      <RouterLink to="/"><StarIcon /> Articles</RouterLink>
      <a href="/" class="socials-mobile-v"><DiscordIcon /> Discord</a>
    </nav>

    <a href="/" class="socials"><DiscordIcon /> Discord</a>
    <Icon
      tabindex="1"
      aria-labelledby="toggle menu"
      @click="show = !show"
      class="burger-menu"
      :icon="
        show
          ? 'line-md:menu-to-close-alt-transition'
          : 'iconamoon:menu-burger-horizontal-bold'
      "
    />
  </header>

  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  line-height: 1.5;
  height: 4rem;
  width: 80%;
  position: absolute;
  border-radius: 5rem;
  background-color: var(--clr-background-primary);
  top: 2rem;
  margin: 0 5%;
  padding-inline: 2rem;
  z-index: 2;
}

.logo {
  display: block;
  width: 5rem;
  height: max-content;
}

nav {
  font-size: 1rem;
  text-align: center;
  display: flex;
  gap: 2rem;
  align-items: center;
}

nav a.router-link-exact-active {
  color: var(--clr-header-navs-hover);
}

nav a.router-link-exact-active:hover,
.socials:hover {
  color: var(--clr-header-navs-hover);
  background-color: var(--clr-header-navs-bg-hover);
}

nav a,
.socials,
.socials-mobile-v {
  display: inline-block;
  padding-inline: 0.8rem;
  border-radius: 2rem;
  color: var(--clr-header-navs);
}

nav a:first-of-type {
  border: 0;
}

.socials,
.socials-mobile-v {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  border: 1px solid var(--clr-header-navs);

  &:hover {
    border: 1px solid var(--clr-header-navs-bg-hover);
  }
}

.socials-mobile-v {
  display: none;
}

.burger-menu {
  display: none;
}

@media screen and (max-width: 1045px) {
  header {
    width: 90%;
  }

  nav {
    gap: 1rem;
  }
}

@media screen and (max-width: 876px) {
  nav {
    display: none;
    position: absolute;
    flex-direction: column;
    right: 0;
    top: 100%;
    width: 50%;
    padding-block: 4rem;
    background-color: var(--clr-background-primary);
    border-radius: 2rem;
  }

  .show-nav {
    display: flex;
  }

  .hide-nav {
    display: none;
  }

  .socials {
    display: none;
  }

  .socials-mobile-v {
    display: flex;
    margin-top: 1.5rem;
  }

  .burger-menu {
    display: block;
    height: 2.5rem;
    width: 4rem;
    color: var(--clr-header-navs);
    outline: none;
    border: none;
  }
}
</style>
