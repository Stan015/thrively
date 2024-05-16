<script setup>
import OurArticlesCardItems from "./OurArticlesCardItems.vue";
</script>

<template>
  <section>
    <h2>OUR Articles</h2>
    <h3>Get Insights and Inspiration</h3>
    <div>
      <OurArticlesCardItems link="/">
        <template #article-img>
          <img src="/60-weigh.svg" alt="60 weigh" />
        </template>
        <template #title>
          <h4>Time & Productivity</h4>
        </template>
        <template #time-read>12 min</template>
        <template #description
          >Dive into a world of inspiration, where and insightful articles,
          practical tools, and there supportive community await you...</template
        >
      </OurArticlesCardItems>

      <OurArticlesCardItems link="/">
        <template #article-img>
          <img src="/elon-m.svg" alt="elon musk" />
        </template>
        <template #title>
          <h4>Adulting Habits</h4>
        </template>
        <template #time-read>24 min</template>
        <template #description
          >Dive into a world of inspiration, where and insightful articles,
          practical tools, and there supportive community await you...</template
        >
      </OurArticlesCardItems>

      <OurArticlesCardItems link="/">
        <template #article-img>
          <img src="/change-the-plan.svg" alt="change the plan" />
        </template>
        <template #title>
          <h4>Change the plan</h4>
        </template>
        <template #time-read>16 min</template>
        <template #description
          >Dive into a world of inspiration, where and insightful articles,
          practical tools, and there supportive community await you...</template
        >
      </OurArticlesCardItems>
    </div>

    <button type="button">&lt;</button>
    <button type="button">&gt;</button>
  </section>
</template>
