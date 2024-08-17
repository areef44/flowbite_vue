<script setup lang="ts">

defineProps<{
  toggleButton: boolean;
  deviceType: 'mobile' | 'tablet' | 'desktop'
}>();
    
</script>

<template>
    <div :class="{
    'sm:ml-0': deviceType === 'mobile' && !toggleButton, 
    'ml-64': deviceType === 'desktop' && !toggleButton,
    'tablet-class': deviceType === 'tablet' && !toggleButton }" 
    class="p-4 dark:bg-gray-800 h-screen">
      <div class="p-4 border-2 border-gray-200 border-dashed rounded-lg dark:border-white mt-14">
        <div class="bg-white dark:bg-gray-800">
          <h1 class="text-gray-900 dark:text-white">Dark mode</h1>
          <p class="text-gray-600 dark:text-gray-300">
            Lorem ipsum...
          </p>
        </div>
      </div>
   </div>
</template>

  
<style scoped>
  /* Additional styles can be added here */
</style>