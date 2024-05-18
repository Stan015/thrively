<script setup>
import OurArticlesCardItems from "./OurArticlesCardItems.vue";
</script>

<template>
  <section>
    <h2>OUR Articles</h2>
    <h3>Get Insights and Inspiration</h3>
    <div class="cards-container">
      <OurArticlesCardItems link="/">
        <template #article-img>
          <img
            src="/60-weigh.svg"
            alt="60 weigh"
            style="width: 100%; height: 100%; aspect-ratio: 16/9"
          />
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
          <img
            src="/elon-m.svg"
            alt="elon musk"
            style="width: 100%; height: 100%; aspect-ratio: 16/9"
          />
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
          <img
            src="/change-the-plan.svg"
            alt="change the plan"
            style="width: 100%; height: 100%; aspect-ratio: 16/9"
          />
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

    <div class="btns">
      <button type="button">&lt;</button>
      <button type="button">&gt;</button>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  width: 80%;
  align-items: center;
  padding-block: 3rem;
  position: relative;

  & h2 {
    font-size: 1.3rem;
    color: var(--clr-heading-third);
    text-transform: uppercase;
    font-weight: 500;
    font-family: Garnett;
    margin-bottom: 1rem;
  }

  & h3 {
    font-size: 2rem;
    font-weight: 500;
    color: var(--clr-heading-primary);
    margin-bottom: 3rem;
    text-align: center;
  }
}

.cards-container {
  display: flex;
  gap: 3rem;
  width: 100%;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin-bottom: 1rem;

  @media screen and (min-width: 1200px) {
    justify-content: space-between;
  }
}

h4 {
  font-size: 1.4rem;
  font-weight: 500;
  color: var(--clr-heading-primary);
}

& .btns {
  display: flex;
  gap: 2rem;
  position: absolute;
  bottom: 0;
  right: 0;
  font-size: 1rem;

  & button {
    background-color: unset;
    width: 2.5rem;
    height: 2.5rem;
    border-radius: 50%;
    border: 1px solid var(--clr-border-primary);
    color: var(--clr-text-black);

    &:hover {
      border: 1px solid var(--clr-border-action);
      background-color: var(--clr-background-third);
      color: var(--clr-text-secondary);
    }
  }
}

@media screen and (max-width: 1045px) {
  section {
    width: 90%;
  }

  & .btns {
    right: unset;
    width: 100%;
    justify-content: center;
  }
}

@media screen and (max-width: 768px) {
}
</style>
