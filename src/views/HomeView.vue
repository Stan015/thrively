<script setup>
import "../assets/main.css";
import HeroSection from "../components/HeroSection.vue";
import OurOffers from "../components/OurOffers.vue";
import OurArticles from "../components/OurArticles.vue";
import FooterSection from "../components/FooterSection.vue";
</script>

<template>
  <HeroSection />
  <main>
    <section class="who-we-are-sect">
      <h2>Who we are?</h2>
      <p>
        We believe in the power of personal development to transform lives. Our
        mission is to provide you with the tools, resources, and support you
        need to unlock your full potential and lead a more fulfilling life.
      </p>
    </section>
    <OurOffers />
    <section class="get-started-sect">
      <div class="container">
        <h3>Get started in just three simple steps</h3>
        <p>
          Subscribe to our newsletter, confirm your subscription, and enjoy
          weekly doses of inspiration, insights, and growth strategies delivered
          straight to your inbox.
        </p>
        <a href="/">Get Started now &gt;</a>
      </div>
      <div class="container-2">
        <div>
          <h4>1</h4>
          <p>Enter your email address and click subscribe on the form</p>
        </div>
        <div>
          <h4>2</h4>
          <p>Check your inbox for a confirmation email</p>
        </div>
        <div>
          <h4>3</h4>
          <p>Once confirmed, you're all set!</p>
        </div>
      </div>
    </section>
    <OurArticles />
  </main>
  <FooterSection />
</template>

<style>
main {
  width: 80%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-inline: 5%;
  padding-top: 4rem;
}

.who-we-are-sect {
  display: flex;
  flex-direction: column;
  gap: 3rem;
  max-width: 45rem;
  height: 18rem;
  padding-top: 2rem;

  & h2 {
    font-size: 1.3rem;
    color: var(--clr-heading-third);
    text-transform: uppercase;
    font-weight: 500;
    font-family: Garnett;
  }

  & p {
    font-size: 1.3rem;
    font-weight: 500;
    font-family: Garnett;
    color: var(--vt-c-dark-purple);
  }
}

.get-started-sect {
  display: flex;
  width: 80%;
  justify-content: space-between;
  gap: 4rem;
  padding-block: 3rem;
  margin-bottom: 3rem;

  & .container {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    width: 23rem;

    & h3 {
      font-size: 2rem;
      font-weight: 500;
      color: var(--clr-heading-primary);
    }

    & p {
      font-size: 1rem;
    }

    & a {
      width: max-content;
      padding: 0.5rem 0.5rem 0.5rem 0;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  & .container-2 {
    display: flex;
    flex-direction: column;
    width: 50%;
    height: 100%;
    justify-content: space-between;

    & div {
      display: flex;
      width: 100%;
      height: 6rem;
      gap: 3rem;
      align-items: center;
      border-bottom: 1px solid var(--clr-border-secondary);
      color: var(--clr-heading-primary);

      & h4 {
        font-size: 1.3rem;
        background-color: var(--clr-background-secondary);
        width: 3rem;
        height: 3rem;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid var(--clr-border-secondary);
        flex-shrink: 0;
      }

      & p {
        font-size: 1.3rem;
      }
    }
  }
}

@media screen and (max-width: 1045px) {
  main {
    width: 90%;
  }
  .who-we-are-sect {
    width: 100%;

    & p {
      font-size: 1.2rem;
    }
  }

  main .get-started-sect {
    width: 100%;
    justify-content: center;
    flex-wrap: wrap;

    & .container {
      justify-content: center;
      width: 70%;
      align-items: center;

      & h3,
      & p {
        text-align: center;
      }
    }
  }
}

@media screen and (max-width: 768px) {
  .get-started-sect {
    & .container-2 {
      width: 70%;
    }
  }
}

@media screen and (max-width: 420px) {
  main .who-we-are-sect {
  height: auto;
  margin-bottom: 2rem;
  }

  main .get-started-sect {
    & .container-2 {
      display: flex;
      flex-direction: column;
      width: 100%;
      height: 100%;
      justify-content: space-between;
      gap: 2rem;

      & div {
        display: flex;
        flex-direction: column;
        width: 100%;
        height: unset;
        gap: 2rem;
        align-items: center;
        padding-block: 1rem;

        & h4 {
          text-align: center;
        }

        & p {
          text-align: center;
        }
      }
    }
  }
}
</style>
