<script setup>
import { ref } from "vue";

const value = ref("");
const handleFormSubmit = () => {
  console.log("thank you for subscribing to our newsletter: " + value.value);
  alert(
    "thank you for subscribing to our newsletter: " +
      value.value +
      " - Don't fret! You are just testing my first vue project and your email isn't subscribed to any newsletter! 🤗"
  );
};
</script>

<template>
  <section class="hero-section">
    <div>
      <h1>Discover Insights, Inspiration & Growth in Every Inbox</h1>
      <p>
        Dive into a world of inspiration, where insightful articles, practical
        tools, and a supportive community await you.
      </p>
    </div>
    <form @submit.prevent="handleFormSubmit">
      <input
        v-model="value"
        type="email"
        name="email"
        id="email"
        required
        placeholder="Enter Your Email"
      />
      <button type="submit">Join the Newsletter</button>
    </form>
    <img
      class="img-1"
      src="/illustrations/female-baker.svg"
      alt="female baker"
    />
    <img
      class="img-2"
      src="/illustrations/man-with-dog.svg"
      alt="man with a dog"
    />
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
  position: relative;
}

.hero-section div {
  width: 60%;
  display: inherit;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1.3rem;
  position: relative;
}

.hero-section div::before {
  content: "";
  width: 3rem;
  height: 3rem;
  background-image: url(/shapes/flower.svg);
  background-repeat: no-repeat;
  position: absolute;
  left: -2rem;
}
.hero-section div::after {
  content: "";
  width: 3rem;
  height: 3rem;
  background-image: url(/shapes/flower.svg);
  background-repeat: no-repeat;
  position: absolute;
  right: -3rem;
  bottom: -3rem;
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
  z-index: 1;
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
  cursor: pointer;
}

.img-1,
.img-2 {
  position: absolute;
  bottom: 0rem;
  width: 20rem;
  height: 20rem;
}

.img-1 {
  left: -1rem;
  bottom: -1rem;
}

.img-2 {
  right: 0rem;
}

@media screen and (max-width: 1045px) {
  h1 {
    font-size: 3rem;
  }

  .img-1,
  .img-2 {
    bottom: 0rem;
    width: 15rem;
    height: 15rem;
  }
}

@media screen and (max-width: 768px) {
  h1 {
    font-size: 2.5rem;
  }

  .img-1,
  .img-2 {
    bottom: 0rem;
    width: 7rem;
    height: 7rem;
  }
}

@media screen and (max-width: 600px) {
  .hero-section div {
    width: 100%;
    padding-inline: 1rem;
  }

  h1 {
    font-size: 2rem;
  }

  p {
    font-size: 1.3rem;
  }

  input {
    width: 20rem;
    padding-inline: 1rem;
  }

  button {
    width: 7rem;
    font-size: 0.8rem;
  }
}

@media screen and (max-width: 380px) {
  h1 {
    font-size: 1.7rem;
  }
}
.hero-section div::before {
  left: 3rem;
}
.hero-section div::after {
  right: 3rem;
}
</style>
