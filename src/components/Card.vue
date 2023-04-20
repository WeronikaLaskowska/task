<template>
  <div
    class="card"
    :class="direction === 'normal' ? 'card--normal' : 'card--reversed'"
  >
    <div class="card__image-wrapper">
      <img class="card__image-wrapper__image" :src="url" alt="" />
      <div class="card__image-wrapper__heart">
        <img src="../assets/heart.png" alt="" />
      </div>
    </div>
    <div class="card__text-section">
      <div class="card__text-section__title">{{ title }}</div>
      <div class="card__text-section__subtitle">{{ subtitle }}</div>
      <a :href="link" target="_blank" class="card__text-section__link">
        <span class="card__text-section__link__text">{{ link_text }}</span>
        <div class="card__text-section__link__arrow"></div>
      </a>
    </div>
  </div>
</template>

<script lang="ts" setup>
interface CardProps {
  title: string;
  subtitle: string;
  url: string;
  link: string;
  link_text: string;
  direction: "normal" | "reverse";
}
const props = defineProps<CardProps>();
</script>

<style lang="scss" scoped>
@use "../scss/card.scss";
</style>
