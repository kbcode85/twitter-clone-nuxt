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
          <TwitterLogo />
        </div>
      </nuxt-link>
    </div>

    <div class="mt-2 space-y-2">

      <SidebarItem to="/" title="Home">
        <template #icon>
          <HomeIcon />
        </template>
        <template #name>
          Home
        </template>
      </SidebarItem>

      <SidebarItem to="/explore">
        <template #icon>
          <HashtagIcon />
        </template>
        <template #name>
          Explore
        </template>
      </SidebarItem>


      <SidebarItem to="/notifications">
        <template #icon>
          <BellIcon />
        </template>
        <template #name>
          Notifications
        </template>
      </SidebarItem>

      <SidebarItem to="/messages">
        <template #icon>
          <InboxIcon />
        </template>
        <template #name>
          Messages
        </template>
      </SidebarItem>

      <SidebarItem to="/bookmarks">
        <template #icon>
          <BookmarkIcon />
        </template>
        <template #name>
          Bookmarks
        </template>
      </SidebarItem>

      <SidebarItem to="/lists">
        <template #icon>
          <DocumentTextIcon />
        </template>
        <template #name>
          Lists
        </template>
      </SidebarItem>

      <SidebarItem to="/profile">
        <template #icon>
          <UserIcon />
        </template>
        <template #name>
          Profile
        </template>
      </SidebarItem>

      <SidebarItem to="/more">
        <template #icon>
          <EllipsisHorizontalIcon />
        </template>
        <template #name>
          More
        </template>
      </SidebarItem>

    </div>

  </div>
</template>

<style scoped>

</style>