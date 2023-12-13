<template>
  <div :class="{ 'dark': darkMode }">
    <div class="bg-white dark:bg-dim-900">

      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>

    </div>
  </div>
</template>

<script setup lang="ts">
const darkMode = ref(false)
</script>

<style scoped>
@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr !important;
  }
}
</style>