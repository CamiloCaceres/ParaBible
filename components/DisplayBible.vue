<script setup lang="ts">
const props = defineProps({
  name: String,
  text: String,
  quote: String,
})
</script>

<template>
  <div class="h-96 w-80 shadow-2xl rounded-lg">
    <h1 class="p-2 text-xl text-gray-800 font-bold">
      {{ props.name }}
    </h1>
    <p class="p-2 mx-2 text-left text-gray-600">
      {{ props.text }}
    </p>
    <p class="p-2 text-right mx-2 text-gray-500">
      {{ props.quote }}
    </p>
  </div>
</template>
