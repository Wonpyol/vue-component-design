<template>
  <div>
    <app-header :title="appTitle"></app-header>
    <app-contents :items="items" @renew="renewItems"></app-contents>
  </div>
</template>
<script>
import {defineComponent} from "vue";
import AppHeader from "@/components/AppHeader.vue";
import AppContents from "@/components/AppContents.vue";

export default defineComponent({
  components: {AppContents, AppHeader},
  data() {
    return {
      appTitle: 'Common Approach',
      items: [10, 20, 30],
    }
  },
  methods: {
    renewItems() {
      this.items = [40, 50, 60];
    },
  },
})
</script>
<style scoped>
</style>
