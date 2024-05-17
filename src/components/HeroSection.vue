<script setup>
import { ref } from 'vue';

const value = ref('')
const handleFormSubmit = () => {
  console.log('thank you for subscribing to our newsletter: ' + value.value)
}
</script>

<template>
  <section class="hero-section">
    <div>
      <h1>Discover Insights, Inspiration 
       & Growth in Every Inbox</h1>
      <p>
        Dive into a world of inspiration, where insightful articles, practical tools, and a supportive community await you.
      </p>
    </div>
    <form @submit.prevent="handleFormSubmit">
      <input v-model="value" type="email" name="email" id="email" placeholder="Enter Your Email">
      <button type="submit">Join the Newsletter</button>
    </form>
  </section>
</template>

<style scoped>
.hero-section {
  display: flex;
  flex-direction: column;
  width: 100%;
  min-height: 100svh;
  align-items: center;
  justify-content: center;
  background-color: var(--clr-background-third);
  color: var(--clr-heading-seondary);
  gap: 3rem;
}

.hero-section div {
  width: 60%;
  display: inherit;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1.3rem;
}

h1 {
  font-size: 4rem;
  text-align: center;
  font-family: Garnett;
  font-weight: 600;
  max-width: 60rem;
}

p {
  font-size: 1.5rem;
  text-align: center;
  text-wrap: balance;
}

form {
  position: relative;
  display: flex;
  align-items: center;
}

input {
  width: 30rem;
  height: 3rem;
  border-radius: 5rem;
  padding-inline: 2rem;
  outline: none;
  border: none;
  background-color: var(--clr-background-primary);
  font-size: 0.8rem;
}

button {
  position: absolute;
  right: 5px;
  width: 9rem;
  height: 2.5rem;
  border-radius: 5rem;
  outline: none;
  border: none;
  background-color: var(--clr-action-secondary);
  color: var(--clr-action-third);
}
</style>
