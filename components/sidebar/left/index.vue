<template>
  <div class="h-screen flex-col flex">
    <div
      class="p-2 rounded-full hover:bg-blue-50 dark:hover:bg-white/20 w-min"
      :class="defaultTransition"
    >
      <NuxtLink to="/">
        <div class="w-8 h-8">
          <LogoTwitter />
        </div>
      </NuxtLink>
    </div>
    <div class="mt-2 p-3 space-y-3">
      <SidebarLeftTab active>
        <template #Icon>
          <Icon name="ic:baseline-home" class="iconSize" />
        </template>
        <template #name> Home </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:hashtag" />
        </template>
        <template #name> Explore </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="mdi:bell" />
        </template>
        <template #name> Notifcations </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:inbox-fill" />
        </template>
        <template #name> Messages </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:bookmark-fill" />
        </template>
        <template #name> Bookmarks </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:file-list-2-fill" />
        </template>
        <template #name> Lists </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:user-3-fill" />
        </template>
        <template #name> Profile </template>
      </SidebarLeftTab>
      <SidebarLeftTab>
        <template #Icon>
          <Icon name="ri:more-fill" />
        </template>
        <template #name> More </template>
      </SidebarLeftTab>
    </div>
  </div>
</template>

<script setup>
const { defaultTransition } = useTailwindConfig();
</script>
