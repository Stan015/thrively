<script setup>
import OurOffersItems from "./OurOffersItems.vue";
import IconPersonalGuidiance from "./icons/IconPersonalGuidiance.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import DailyNewsletterIcon from "./icons/IconDailyNewsletter.vue";
// import ArrowForwardIcon from "./icons/ArrowForward.vue"
</script>

<template>
  <div class="container-div">
    <h2>Our Offers</h2>
    <h3>What you get from Thrively</h3>

    <div class="first-div">
      <OurOffersItems>
        <template #icon>
          <DailyNewsletterIcon />
        </template>
        <template #heading>Daily Newsletter</template>
        <template #paragraph>
          Newsletter packed with insights, tips, and motivation tailored to fuel
          your personal growth journey every day.
        </template>
      </OurOffersItems>
      <OurOffersItems>
        <template #icon>
          <IconPersonalGuidiance />
        </template>
        <template #heading>Personal Guidance</template>
        <template #paragraph>
          Resources that provides you with practical tools and strategies to set
          and achieve your goals effectively.
        </template>
      </OurOffersItems>
      <OurOffersItems>
        <template #icon>
          <CommunityIcon />
        </template>
        <template #heading>Community</template>
        <template #paragraph
          >A supportive community, where like-minded individuals come together
          to share experiences.</template
        >
      </OurOffersItems>
    </div>

    <div class="second-div">
      <div class="container item1">
        <img
          src="/illustrations/women-spa-treatment.svg"
          alt="illustration of woman doing spa treatment"
        />
        <div>
          <h3>Growth in Every Inbox</h3>
          <p>
            Receive curated content, expert insights, and actionable tips
            delivered straight to your inbox, empowering you to grow personally
            and socially with each message.
          </p>
          <a href="/">Learn more &gt;</a>
        </div>
      </div>
      <div class="container item2">
        <div>
          <h3>Community Connection</h3>
          <p>
            Engage with fellow subscribers, share your experiences, and foster
            meaningful connections as you journey towards self-improvement
            together.
          </p>
          <a href="/">Learn more &gt;</a>
        </div>
        <img
          src="/illustrations/man-celebrates.svg"
          alt="illustration of man celebrating"
        />
      </div>
      <div class="container">
        <img
          src="/illustrations/female-baker.svg"
          alt="illustration of woman doing spa treatment"
        />
        <div>
          <h3>FInd What You Love</h3>
          <p>
            From career advice to mindfulness practices, our newsletter covers a
            wide range of subjects, ensuring you find inspiration and enjoyment
            in every issue.
          </p>
          <a href="/">Learn more &gt;</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container-div {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--clr-background-secondary);
  border: 2px solid var(--clr-border-primary);
  border-radius: 4rem;
  padding: 6rem;
  margin-bottom: 4rem;
}

h2 {
  font-size: 1.3rem;
  color: var(--clr-heading-third);
  text-transform: uppercase;
  font-weight: 500;
  font-family: Garnett;
  margin-bottom: 1rem;
}

h3 {
  font-size: 2rem;
  font-weight: 500;
  color: var(--clr-heading-primary);
  text-align: center;
}

.first-div,
.second-div {
  width: 100%;
  display: flex;
  gap: 2rem;
  justify-content: center;
  align-items: center;
  padding-block: 3rem;
  flex-wrap: wrap;
}

.first-div {
  margin-block: 3rem;
}

.second-div {
  flex-direction: column;
  border-top: 2px solid var(--clr-border-secondary);
  gap: 5rem;
  padding-block: 6rem;

  & .container {
    display: inherit;
    justify-content: space-between;
    width: 100%;
    gap: 2rem;
    position: relative;
    flex-wrap: wrap;

    & img {
      height: 15rem;
      width: 15rem;
    }

    & div {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      & p {
        width: 20rem;
      }

      & a {
        width: max-content;
        padding: 0.5rem 0.5rem 0.5rem 0;
      }
      & a:hover {
        text-decoration: underline;
      }
    }
  }
  .item1::before {
    content: "";
    width: 6rem;
    height: 5rem;
    background-image: url(/shapes/curly-arrow-left.svg);
    background-repeat: no-repeat;
    position: absolute;
    left: 40%;
    bottom: -2rem;
  }
  .item2::before {
    content: "";
    width: 6rem;
    height: 5rem;
    background-image: url(/shapes/curly-arrow-right.svg);
    background-repeat: no-repeat;
    position: absolute;
    left: 40%;
    bottom: -2rem;
  }
}
@media screen and (max-width: 1045px) {
  .container-div {
    border-radius: 4rem;
    padding: 4rem;
    margin-bottom: 4rem;
  }
}

@media screen and (max-width: 876px) {
  .second-div {
    h3 {
      text-align: center;
      margin-bottom: 1rem;
    }
    & .container {
      justify-content: center;

      & div {
        align-items: center;

        & p {
          width: 18rem;
          text-align: center;
        }

        & a {
          z-index: 1;
        }
      }
    }

    .item1::before {
      left: 30%;
      bottom: -4rem;
    }
    .item2::before {
      left: 30%;
      bottom: -4rem;
    }
  }
}

@media screen and (max-width: 420px) {
  .container-div {
    padding: 2rem;

    & .second-div {
      padding-block: 3rem;
    }
  }
}
</style>
