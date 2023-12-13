<script setup lang="ts">
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  loading: {
    type: Boolean,
    default: true
  }
})
</script>

<template>
  <div>
    <div class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
      <h2 class="text-xl font-bold">{{props.title}}</h2>
    </div>
    <div v-if="loading">
      <h3>Loading...</h3>
    </div>
    <div v-else>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>

</style>