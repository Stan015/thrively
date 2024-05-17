<script setup>
import ClockIcon from "./icons/IconClock.vue";

defineProps({
  link: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="card-container">
    <div class="card">
      <span class="img-container">
        <slot class="img" name="article-img"></slot>
      </span>
      <div class="card-title">
        <slot name="title"></slot>
        <span class="time-read">
          <i class="icon"><ClockIcon /></i>
          <slot name="time-read"></slot>
        </span>
      </div>
      <p><slot name="description"></slot></p>
      <a :href="link">Read Now &gt;</a>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  position: relative;
}

.card {
  display: flex;
  flex-direction: column;
  width: 20rem;
  height: 28rem;
  border-radius: 1rem;
  border: 1px solid var(--clr-border-primary);
  padding: 1rem;
  gap: 2rem;
  justify-content: space-between;
  align-items: center;

  & .img-container {
    width: 100%;
    height: 10.2rem;
    border: 1px solid var(--clr-border-primary);
    border-radius: 1rem;
    overflow: hidden;
    display: flex;
    align-items: center;
  }

  & .card-title {
    display: flex;
    width: 100%;
    justify-content: space-between;
    font-size: 1rem;

    & .time-read {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      font-size: 1rem;

      & i {
        width: 1rem;
        height: 1rem;
      }
    }
  }

  & p {
    font-size: 0.8rem;
    width: 100%;
    font-family: Garnett;
    color: var(--clr-text-primary);
  }

  & a {
    width: 90%;
    height: 2.5rem;
    border: 1px solid var(--clr-border-action);
    border-radius: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: center;

    &:hover {
      background-color: var(--clr-background-third);
      color: var(--clr-text-secondary);
    }
  }
}
</style>
