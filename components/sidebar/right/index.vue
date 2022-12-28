<template>
  <div class="flex flex-col">
    <!-- Preview Card: What's happening -->
    <SidebarRightPreviewCard title="What's Happening">
      <SidebarRightPreviewCardItem
        v-for="whatsHappening in WhatsHappeningItems"
      >
        <div>
          <h2>{{ whatsHappening.title }}</h2>
          <p>{{ whatsHappening.count }}</p>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
    <!-- Preview CardL Who to Follow -->
    <SidebarRightPreviewCard title="Who to Follow">
      <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
        <div class="flex items-center flex-row justify-between p-2">
          <div class="flex flex-row">
            <img
              class="w-10 h-10 rounded-full"
              :src="whoToFollow.image"
              :alt="whoToFollow.name"
            />
            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h1>
              <p class="text-xs text-gray-600">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full bg-black dark:bg-white rounded-full">
            <button
              class="px-4 py-2 font-bold tex-xs text-white dark:text-black"
            >
              Follow
            </button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>
<script setup>
const WhatsHappeningItems = ref([
  {
    title: "Space X",
    count: "18.8k Twewets",
  },
  {
    title: "#CodingIsFun",
    count: "18.8k Twewets",
  },
  {
    title: "Space X",
    count: "18.8k Twewets",
  },
]);

const whoToFollowItems = ref([
  {
    name: "Ruby on Rails Tutorial",
    handle: "18.8k Twewets",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Vue School",
    handle: "18.8k Twewets",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Nuxt Labs",
    handle: "18.8k Twewets",
    image: "https://picsum.photos/200/200",
  },
]);
</script>
