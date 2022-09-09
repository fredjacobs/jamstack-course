<script setup>
defineProps({
  blok: Object,
});
</script>

<template>
  <div class="conatainer" v-editable="blok">
    <h1 style="margin-left: 10px">{{ blok.title }}</h1>
    <div class="featured-projects">
      <div class="project" v-for="project in blok.project" :key="project._uid">
        <NuxtLink
          :to="{ name: 'projects-slug', params: { slug: project.slug } }"
        >
          <img
            :src="project.content.image?.filename"
            :alt="project.image?.alt"
          />
          <h3>{{ project.content.name }}</h3>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>
