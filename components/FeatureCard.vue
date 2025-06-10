<template>
  <div class="bg-white rounded-lg shadow-md p-6 flex-1 text-center">
    <!-- لوگو -->
    <img
      v-if="icon"
      :src="icon"
      alt="آیکن ویژگی"
      class="mx-auto mb-4 w-16 h-16 object-contain"
    />
    <h3 class="text-2xl font-semibold text-gray-800 mb-2">{{ title }}</h3>
    <p class="text-gray-600">{{ description }}</p>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  icon: String,
});
</script>
