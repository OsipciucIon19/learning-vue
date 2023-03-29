<template>
  <div>
    <TheHeader :title="title" />
    <TheResources />
  </div>
</template>

<script>
import TheHeader from "@/components/layouts/TheHeader.vue";
import TheResources from "@/components/learing-resources/TheResources.vue";

export default {
  name: 'App',
  components: {
    TheResources,
    TheHeader
  },
  data() {
    return {
      title: 'RememberMe'
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'Roboto', sans-serif;
}

body {
  margin: 0;
}
</style>
