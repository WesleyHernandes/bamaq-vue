<template>
  <main class="app">
    <router-view />
  </main>
</template>

<script setup lang="ts">
defineOptions({
  name: 'MainLayout',
});
</script>

<style scoped>
.app {
  display: flex;
  width: 100%;
  min-height: 100vh;
  flex-direction: column;
}
</style>
