<script setup lang="ts">
import {Bars3Icon, HomeIcon, MagnifyingGlassIcon} from "@heroicons/vue/24/solid"
</script>

<template>
  <div class="fixed bottom-0 w-full bg-white dark:bg-dim-900 dark:text-white md:hidden border-t border-gray-300 dark:border-white/20">
    <div class="flex justify-around py-2">
      <button @click="openSidebar">
        <Bars3Icon class="h-12 w-12"/>
      </button>
      <button @click="showHome">
        <HomeIcon class="h-12 w-12"/>
      </button>
      <button @click="showSearch">
        <MagnifyingGlassIcon class="h-12 w-12"/>
      </button>
    </div>
  </div>
</template>

<style scoped>

</style>