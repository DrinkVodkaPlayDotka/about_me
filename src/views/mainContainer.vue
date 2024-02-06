<script lang="ts">
import { defineComponent } from 'vue'
import BackgroundComponent from "@/components/backgroundComponent.vue";
import MeComponent from "@/components/meComponent.vue";

export default defineComponent({
  components: {
    MeComponent,
    BackgroundComponent

  }
})
</script>

<template>
  <background-component />
  <me-component></me-component>
</template>

<style scoped></style>
