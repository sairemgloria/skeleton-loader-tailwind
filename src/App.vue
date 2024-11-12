<script setup>
import { ref, onMounted } from 'vue';

const loading = ref(true);

// Simulate content loading (e.g., API call or async data loading)
onMounted(() => {
  setTimeout(() => {
    loading.value = false;
  }, 2000); // adjust this delay to match actual loading time
});
</script>

<template>
  <div>
    <div v-if="loading">
      <!-- Skeleton loader content -->
      <div class="skeleton h-32 w-32"></div>
    </div>
    <div v-else>
      <!-- Actual content -->
      <img class="mask mask-square" src="/public/images/ConsolePNG.png" />
    </div>
  </div>
</template>

<style scoped>

</style>
