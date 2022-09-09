<script setup>
const story = await useStoryblok(
  "home",
  {
    version: "draft",
    resolve_relations: "featuredProjects.project",
  },
  {
    resolveRelations: "featureProjects.project",
  }
);
</script>

<template>
  <div>
    <StoryblokComponent v-if="story" :blok="story.content"></StoryblokComponent>
  </div>
</template>
