<template>
  <div>
    <BaseCard>
      <base-button
        @click="setSelectedTab('stored-resources')"
        :mode="selectedTab === 'stored-resources' ? null : 'flat'"
      >Stored Resources</base-button>
      <base-button
        @click="setSelectedTab('add-learning-resource')"
        :mode="selectedTab === 'add-learning-resource' ? null : 'flat'"
      >Add Resource</base-button>
    </BaseCard>
    <component :is="selectedTab"></component>
  </div>
</template>

<script>
import BaseCard from "@/components/UI/BaseCard.vue";
import BaseButton from "@/components/UI/BaseButton.vue";
import StoredResources from "@/components/learing-resources/StoredResources.vue";
import AddLearningResource from "@/components/learing-resources/AddLearningResource.vue";

export default {
  name: "TheResources",
  components: {BaseButton, BaseCard, StoredResources, AddLearningResource},
  data() {
    return {
      count: 0,
      selectedTab: 'stored-resources',
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue.js documentation',
          link: 'https://vuejs.org'
        },
        {
          id: 'google',
          title: 'Google',
          description: 'The official Google documentation',
          link: 'https://google.com'
        },
      ]
    }
  },
  provide() {
    return {
      resources: this.storedResources
    }
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab
    }
  }
}
</script>

<style scoped>

</style>