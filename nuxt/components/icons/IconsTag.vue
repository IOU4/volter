<script setup lang="ts">
interface Props {
  stroke?: string
}
const { stroke = "stroke-primary-600" } = defineProps<Props>()
</script>
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" fill="#000000" viewBox="0 0 256 256">
    <rect width="256" height="256" fill="none"></rect>
    <path d="M200,176V64a23.9,23.9,0,0,0-24-24H40" fill="none" :class="stroke" stroke-linecap="round"
      stroke-linejoin="round" stroke-width="12"></path>
    <path d="M22.1,80A24,24,0,1,1,64,64V192a24,24,0,1,0,41.9-16h112A24,24,0,0,1,200,216H88" fill="none" :class="stroke"
      stroke-linecap="round" stroke-linejoin="round" stroke-width="12"></path>
  </svg>
</template>




