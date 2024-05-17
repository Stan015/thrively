<script setup>
const pages = { Books: "/", Documentry: "/", Careers: "/", Articles: "/" };
const follow = { Discord: "/", Twitter: "/", Instagram: "/", Medium: "/" };
const legals = { Privacy: "/", Contract: "/", Support: "/" };

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
  <section>
    <div class="ftr-container">
      <div class="first-child-div">
        <div class="subscription-div">
          <h2>Subscribe to our Newsletter</h2>
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
        </div>
        <div class="quick-links">
          <div>
            <h5>Pages</h5>
            <ul>
              <li v-for="(value, key, index) in pages" :key="index">
                <a :href="value">{{ key }}</a>
              </li>
            </ul>
          </div>
          <div>
            <h5>Follow</h5>
            <ul>
              <li v-for="(value, key, index) in follow" :key="index">
                <a :href="value">{{ key }}</a>
              </li>
            </ul>
          </div>
          <div>
            <h5>Legals</h5>
            <ul>
              <li v-for="(value, key, index) in legals" :key="index">
                <a :href="value">{{ key }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="second-child-div">
        <p>
          &copy;
          <a href="https://twitter.com/StanleyAzi" target="_blank"
            >Stanley Azi (Frontend Dev)</a
          >
          &
          <a href="https://twitter.com/Austine_Ifenna" target="_blank"
            >Austine Ifenna (Web Designer)</a
          >
        </p>
        <a href="/">Terms and Condition</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  display: block;
  width: 100%;
  padding: 2rem;
  margin-top: 3rem;
}

.ftr-container {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  width: 100%;
  background-color: var(--clr-background-third);
  color: var(--clr-text-secondary);
  border-radius: 2rem;
  padding: 3rem 2rem 2rem 2rem;
}

.ftr-container .first-child-div {
  display: flex;
  width: 100%;
  justify-content: space-between;

  & .subscription-div {
    display: flex;
    flex-direction: column;
    gap: 3rem;
    width: 20rem;
    position: relative;

    & h2 {
      font-size: 2rem;
      font-family: Garnett;
    }

    form {
      position: relative;
      display: flex;
      align-items: center;
      width: 100%;
    }

    input {
      width: 100%;
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
      width: 8rem;
      height: 2.5rem;
      border-radius: 5rem;
      outline: none;
      font-size: 0.7rem;
      border: none;
      background-color: var(--clr-action-secondary);
      color: var(--clr-action-third);
      cursor: pointer;
    }
  }
  .subscription-div::after {
  content: '';
  width: 3rem;
  height: 3rem;
  background-image: url(/shapes/flower.svg);
  background-repeat: no-repeat;
  position: absolute;
  right: -4rem;
  bottom: 3rem;
  transform: scale(-1, 1)
}

  & .quick-links {
    display: flex;
    width: max-content;
    gap: 2rem;
    margin-right: 2rem;

    & div {
      display: block;

      & h5 {
        font-size: 1rem;
        font-family: Garnett;
      }

      & ul {
        margin-top: 1rem;
        padding: 0;
        display: flex;
        flex-direction: column;
        gap: 0.5rem;

        & li {
          margin: 0;

          & a {
            color: var(--clr-text-secondary);
            margin: 0;
            padding: 0;
            font-size: 0.8rem;

            &:hover {
              text-decoration: underline;
            }
          }
        }
      }
    }
  }
}

.ftr-container .second-child-div {
  display: flex;
  width: 100%;
  justify-content: space-between;
  gap: 2rem;
  height: 4rem;
  align-items: center;
  border-top: 1px solid var(--clr-border-secondary);
  margin-top: 2rem;

  & a {
    color: var(--clr-text-secondary);
    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
