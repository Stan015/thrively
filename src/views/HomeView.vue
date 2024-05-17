<script setup>
import '../assets/main.css'
import HeroSection from "../components/HeroSection.vue";
import OurOffers from "../components/OurOffers.vue";
import OurArticles from "../components/OurArticles.vue";
import FooterSection from "../components/FooterSection.vue";
</script>

<template>
  <HeroSection />
  <main>
    <section>
      <h3>Who we are?</h3>
      <p>
        We believe in the power of personal development to transform lives. Our
        mission is to provide you with the tools, resources, and support you
        need to unlock your full potential and lead a more fulfilling life.
      </p>
    </section>
    <OurOffers />
    <section>
      <div>
        <h3>Get started in just three simple steps</h3>
        <p>Subscribe to our newsletter, confirm your subscription, and enjoy weekly doses of inspiration, insights, and growth strategies delivered straight to your inbox.</p>
        <a href="/">Get Started now &gt;</a>
      </div>
      <div>
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
    <FooterSection />
  </main>
</template>
