<script lang="ts">
import { defineComponent } from 'vue'
import BackgroundComponent from "@/components/backgroundComponent.vue";
import MeComponent from "@/components/meComponent.vue";
import AboutmeComponent from "@/components/aboutmeComponent.vue";
import HeadComponent from "@/components/headComponent.vue";
import StarComponent from "@/components/starComponent.vue";

export default defineComponent({
  components: {
    StarComponent,
    HeadComponent,
    AboutmeComponent,
    MeComponent,
    BackgroundComponent

  }
})
</script>

<template>
  <star-component></star-component>
  <background-component />
  <head-component></head-component>
  <me-component></me-component>
  <aboutme-component></aboutme-component>
</template>

<style scoped></style>
