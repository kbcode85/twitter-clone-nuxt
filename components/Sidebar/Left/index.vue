<script setup lang="ts">
import { HomeIcon } from "@heroicons/vue/24/solid"
import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, EllipsisHorizontalIcon, PencilIcon, ChevronDownIcon } from "@heroicons/vue/24/outline"

const { defaultTransition } = useTailwindConfig()
</script>

<template>
 <div class="flex flex-col h-screen">

   <div class="p-2 my-2 rounded-full hover:bg-blue-50 w-min dark:hover:bg-white/20">
      <nuxt-link to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </nuxt-link>
   </div>

   <div class="mt-2 space-y-2">

     <SidebarLeftTab active>
       <template #icon>
         <HomeIcon />
       </template>
       <template #name>
         Home
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <HashtagIcon />
       </template>
       <template #name>
         Explore
       </template>
     </SidebarLeftTab>


     <SidebarLeftTab>
       <template #icon>
         <BellIcon />
       </template>
       <template #name>
         Notifications
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <InboxIcon />
       </template>
       <template #name>
         Messages
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <BookmarkIcon />
       </template>
       <template #name>
         Bookmarks
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <DocumentTextIcon />
       </template>
       <template #name>
         Lists
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <UserIcon />
       </template>
       <template #name>
         Profile
       </template>
     </SidebarLeftTab>

     <SidebarLeftTab>
       <template #icon>
         <EllipsisHorizontalIcon />
       </template>
       <template #name>
         More
       </template>
     </SidebarLeftTab>

   </div>

 </div>
</template>

<style scoped>

</style>