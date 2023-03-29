<template>
  <ul>
    <LearningResource
      v-for="resource in resources"
      :key="resource.id"
      :title="resource.title"
      :description="resource.description"
      :link="resource.link"
    />
  </ul>
</template>

<script>
import LearningResource from "@/components/learing-resources/LearningResource.vue";

export default {
  name: "StoredResources",
  components: {
    LearningResource
  },
  inject: ['resources']
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: auto;
  padding: 0;
  max-width: 40rem;
}
</style>