<template>
  <NuxtLink
    class="flex text-gray-800 items-center justify-center h-min w-min p-2 hover:bg-gray-200 rounded-full dark:hover:bg-dim-200 dark:text-white"
    to="#"
    :class="defaultTransiton"
  >
    <div class="text-dark">
      <slot name="Icon"> </slot>
    </div>
    <div class="hidden ml-4 text-md xl:block" :class="textClasses">
      <slot name="name">a</slot>
    </div>
  </NuxtLink>
</template>

<script setup>
const { defaultTransiton } = useTailwindConfig();

const props = defineProps({
  active: {
    type: Boolean,
    default: false,
  },
});

const textClasses = computed(() =>
  props.active ? "font-semibold" : "font-normal"
);
</script>
