<script setup>
import "./assets/main.css";
import { RouterLink, RouterView } from "vue-router";
import StarIcon from "./components/icons/IconStar.vue";
import DiscordIcon from "./components/icons/IconDiscord.vue";
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

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/">Books</RouterLink>
      <RouterLink to="/">Documentary</RouterLink>
      <RouterLink to="/">Careers</RouterLink>
      <RouterLink to="/"><StarIcon /> Articles</RouterLink>
    </nav>

    <a href="/" class="socials"><DiscordIcon /> Discord</a>
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
  margin: 0 10%;
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
.socials {
  display: inline-block;
  padding-inline: 0.8rem;
  border-radius: 2rem;
  color: var(--clr-header-navs);
}

nav a:first-of-type {
  border: 0;
}

.socials {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}

@media screen and (max-width: 1045px) {
  header {
    width: 90%;
  }

  nav {
    gap: 1rem;
  }
}

@media screen and (max-width: 768px) {
  nav {
    display: none;
  }
}
</style>
