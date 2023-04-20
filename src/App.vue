<script setup lang="ts">
import Card from "./components/Card.vue";
import { data } from "./data/mockup";
</script>

<template>
  <div class="container">
    <Card
      v-for="({ title, subtitle, link, image, id, link_text }, index) in data"
      :key="id"
      :title="title"
      :subtitle="subtitle"
      :link_text="link_text"
      :url="image"
      :link="link"
      :direction="index % 2 == 0 ? 'normal' : 'reverse'"
    ></Card>
  </div>
</template>

<style lang="scss" scoped>
@use "./scss/container.scss";
</style>
