<script setup>
import OurOffersItems from "./OurOffersItems.vue";
import IconPersonalGuidiance from "./icons/IconPersonalGuidiance.vue";
import CommunityIcon from "./icons/IconCommunity.vue";
import DailyNewsletterIcon from "./icons/IconDailyNewsletter.vue";
// import ArrowForwardIcon from "./icons/ArrowForward.vue"
</script>

<template>
  <h2>Our Offers</h2>
  <h3>What you get from Thrively</h3>

  <div>
    <OurOffersItems>
      <template #icon>
        <DailyNewsletterIcon />
      </template>
      <template #heading>Daily Newsletter</template>
      Newsletter packed with insights, tips, and motivation tailored to fuel your
      personal growth journey every day.
    </OurOffersItems>
    <OurOffersItems>
      <template #icon>
        <IconPersonalGuidiance />
      </template>
      <template #heading>Personal Guidance</template>
      Resources that provides you with practical tools and strategies to set and
      achieve your goals effectively.
    </OurOffersItems>
    <OurOffersItems>
      <template #icon>
        <CommunityIcon />
      </template>
      <template #heading>Community</template>
      A supportive community, where like-minded individuals come together to share
      experiences.
    </OurOffersItems>
  </div>

  <div>
    <div>
      <img src="/illustrations/women-spa-treatment.svg" alt="illustration of woman doing spa treatment">
      <div>
        <h3>Growth in Every Inbox</h3>
        <p>Receive curated content, expert insights, and actionable tips delivered straight to your inbox, empowering you to grow personally and socially with each message.</p>
        <a href="/">Learn more &gt;</a>
      </div>
    </div>
    <div>
      <img src="/illustrations/man-celebrates.svg" alt="illustration of man celebrating">
      <div>
        <h3>Community Connection</h3>
        <p>Engage with fellow subscribers, share your experiences, and foster meaningful connections as you journey towards self-improvement together.</p>
        <a href="/">Learn more &gt;</a>
      </div>
    </div>
    <div>
      <img src="/illustrations/female-baker.svg" alt="illustration of woman doing spa treatment">
      <div>
        <h3>FInd What You Love</h3>
        <p>From career advice to mindfulness practices, our newsletter covers a wide range of subjects, ensuring you find inspiration and enjoyment in every issue.</p>
        <a href="/">Learn more &gt;</a>
      </div>
    </div>
  </div>
</template>
