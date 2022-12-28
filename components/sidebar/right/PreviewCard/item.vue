<template>
  <div
    class="p-3 hover:bg-gray-100 cursor-pointer dark:hover:bg-dim-300 border-b"
    :class="wrapperClasses"
  >
    <slot> aa</slot>
  </div>
</template>

<script setup>
const wrapperClasses = computed(
  () => `${TwitterBorderColor} ${defaultTransition}`
);
const { TwitterBorderColor, defaultTransition } = useTailwindConfig();
</script>
