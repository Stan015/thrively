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
  <div>
    <div class="card-container">
      <div class="card">
        <div class="article-img">
          <slot name="article-img"></slot>
        </div>
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
  </div>
</template>
