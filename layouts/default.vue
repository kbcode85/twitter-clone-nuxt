<script setup lang="ts">

</script>

<template>
  <div class="min-h-full">
    <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-5">

    <div class="md:block xs-col-span-1 xl:col-span-2">
      <div class="sticky top-0">
        <Sidebar />
      </div>
    </div>

    <main class="col-span-12 xl:col-span-6 md:col-span-8">
      <router-view />
    </main>

    <div class="md:block xl:col-span-4 md:col-span-3">
      <div class="sticky top-0">
        <AsideSection />
      </div>
    </div>

    </div>
  </div>
</template>

<style scoped>

</style>