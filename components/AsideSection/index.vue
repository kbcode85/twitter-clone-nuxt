<script setup lang="ts">
import { MagnifyingGlassIcon } from '@heroicons/vue/24/outline';

const whatsHappeningItems = ref([
  {
    title: 'Brauna',
    count: '18.8k posts'
  },
  {
    title: 'sejmie',
    count: '8.8k posts'
  },
  {
    title: 'Żydów',
    count: '1.8k posts'
  }
])

const whoToFollowItems = ref([
  {
    name: 'Grzegorz Braun',
    handle: '@BraunGrzegorz',
    image: 'https://ocdn.eu/pulscms-transforms/1/iD5k9kpTURBXy9lZDgwM2Q5ZGM1NTQ5MGFhZjM0NGEyMmYwMDhhNWI3Ni5qcGeSlQMAzFPNB9DNBGWTBc0HMM0DmN4AAqEwBqExAQ'
  },
  {
    name: 'Krzysztof Bosak',
    handle: '@KrzysztofBosak',
    image: 'https://img.dorzeczy.pl/img/wicemarszalek-sejmu-krzysztof-bosak/13/5b/f568f10c1fc18e2ff6e5c52e8286.jpeg'
  },
  {
    name: 'Janusz Korwin-Mikke',
    handle: '@KorwinMikke',
    image: 'https://i.gremicdn.pl/image/free/3ad5bfccb17b9abd7855be2610518015/?t=crop:2186:1355:nowe:63.709677419355:398.5,resize:fill:1200:716,enlarge:1'
  }
])

</script>

<template>
  <div class="flex flex-col">

    <!-- Search bar -->
    <div class="relative m-2">
      <div class="absolute flex items-center h-full pl-4 text-gray-600 cursor-pointer">
        <div class="w-6 h-6">
          <MagnifyingGlassIcon @click="handleSearch" />
        </div>
      </div>
      <input v-model="search"
             class="flex items-center w-full pl-12 text-sm font-normal text-black bg-gray-200 border border-gray-200 rounded-full shadow dark:text-gray-100 dark:bg-dim-400 dark:border-dim-400 focus:bg-gray-100 dark:focus:bg-dim-900 focus:outline-none focus:border focus:border-blue-200 h-9"
             placeholder="Search tweet" type="text">
    </div>

    <!-- Who to follow -->
    <AsideSectionPreview title="Who to follow">
      <AsideSectionPreviewItem v-for="whoToFollow in whoToFollowItems">
        <div class="flex flex-row items-center justify-between p-2">
          <div class="flex flex-row">
            <img class="w-10 h-10 rounded-full object-cover" :src="whoToFollow.image" :alt="whoToFollow.name">

            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button
                class="px-4 py-2 text-xs font-bold text-white bg-black rounded-full dark:text-black dark:bg-white">Follow</button>
          </div>
        </div>
      </AsideSectionPreviewItem>
    </AsideSectionPreview>


    <!-- Trends -->
    <AsideSectionPreview title="Trends">

      <AsideSectionPreviewItem v-for="whatsHappening in whatsHappeningItems">
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>

          <p class="text-xs text-gray-400">
            {{ whatsHappening.count }}
          </p>
        </div>
      </AsideSectionPreviewItem>

    </AsideSectionPreview>

    <!-- Footer-->
    <footer>
      <ul class="mx-2 my-4 text-xs text-gray-500">
        <li class="inline-block mx-2">
          <a href="#" class="hover:underline" @click.prevent="handleToggleDarkMode">Dark mode</a>
        </li>
        <li class="inline-block mx-2">
          <a href="https://github.com/kbcode85/twitter-clone-nuxt" target="_blank" class="hover:underline">Github</a>
        </li>
        <li class="inline-block mx-2">
          Twitter Clone
        </li>
        <li class="inline-block mx-2">
          Nuxt + Tailwind CSS + Prisma
        </li>
        <li class="inline-block mx-2">
          Projekt na zaliczenie
        </li>
      </ul>
    </footer>

  </div>
</template>

<style scoped>

</style>