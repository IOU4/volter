<script setup lang="ts">
interface Props {
  stroke?: string
}
const { stroke = "stroke-primary-600" } = defineProps<Props>()
</script>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#000000" viewBox="0 0 256 256">
    <rect width="256" height="256" fill="none"></rect>
    <circle cx="116" cy="116" r="84" fill="none" :class="stroke" stroke-linecap="round" stroke-linejoin="round"
      stroke-width="12"></circle>
    <line x1="175.4" y1="175.4" x2="224" y2="224" fill="none" :class="stroke" stroke-linecap="round"
      stroke-linejoin="round" stroke-width="12"></line>
  </svg>
</template>

