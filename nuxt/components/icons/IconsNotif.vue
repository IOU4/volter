<script setup lang="ts">
interface Props {
  stroke?: string
}
const { stroke = "stroke-primary-600" } = defineProps<Props>()
</script>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#000000" viewBox="0 0 256 256">
    <rect width="256" height="256" fill="none"></rect>
    <line x1="95.9" y1="224" x2="159.9" y2="224" fill="none" :class="stroke" stroke-linecap="round"
      stroke-linejoin="round" stroke-width="12"></line>
    <path
      d="M56.2,104a71.9,71.9,0,0,1,72.3-72c39.6.3,71.3,33.2,71.3,72.9V112c0,35.8,7.5,56.6,14.1,68a8,8,0,0,1-6.9,12H49a8,8,0,0,1-6.9-12c6.6-11.4,14.1-32.2,14.1-68Z"
      fill="none" :class="stroke" stroke-linecap="round" stroke-linejoin="round" stroke-width="12"></path>
  </svg>
</template>
