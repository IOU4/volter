<script setup lang="ts">
const items = ref(await useGetActiveItems());
const refreshItems = async () => {
  items.value = await useGetActiveItems();
}
</script>

<template>
  <div>
    <div class="heading flex justify-between py-4 mb-2">
      <h1 class="text-primary-500 text-lg">Available Items:</h1>
      <IconsSearch class="icon" />
    </div>
    <div class="grid lg:grid-cols-2 gap-y-10 gap-x-4">
      <Item v-for="item in items" :key="item.id" :item="item" @update="refreshItems" />
    </div>
    <div class=" fixed bottom-6 left-0 right-0 w-screen pointer-events-none">
      <nuxt-link to="/items/create"
        class="btn-outline flex space-x-2 hover:bg-white bg-primary-500 mx-auto w-fit group pointer-events-auto">
        <span class="group-hover:text-primary-700 text-white ">create one</span>
        <IconsPlus class="w-6 h-6" stroke="group-hover:stroke-primary-600 stroke-white" />
      </nuxt-link>
    </div>
    <Reserve @upd="refreshItems" />
  </div>
</template>
