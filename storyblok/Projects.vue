<script setup>
defineProps({
  blok: Object,
});
</script>

<template>
  <div class="container project-page">
    <div class="project-title">
      <h1>{{ blok.name || "New Project" }}</h1>
      <NuxtLink :to="{ name: 'index' }">Go Back</NuxtLink>
    </div>

    <div class="project-description">
      <img
        :src="blok.image?.filename || 'https://picsum.photos/200/300'"
        :alt="blok.image?.alt"
      />
      <p>
        {{ blok.description || "Lorum op sy Ipsum is hy nou daar, dankie." }}
      </p>
    </div>
  </div>
</template>
