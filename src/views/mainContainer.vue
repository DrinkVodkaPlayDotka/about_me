<script lang="ts">
import { defineComponent } from 'vue'
import BackgroundComponent from "@/components/backgroundComponent.vue";
import MeComponent from "@/components/meComponent.vue";
import AboutmeComponent from "@/components/aboutmeComponent.vue";
import HeadComponent from "@/components/headComponent.vue";

export default defineComponent({
  components: {
    HeadComponent,
    AboutmeComponent,
    MeComponent,
    BackgroundComponent

  }
})
</script>

<template>
  <background-component />
  <head-component></head-component>
  <me-component></me-component>
  <aboutme-component></aboutme-component>
</template>

<style scoped></style>
