<script setup>
import TheNav from './components/TheNav.vue';
</script>

<template>
  <div class="min-h-full">
    <TheNav />
    <main>
      <router-view></router-view>
    </main>
</div>
</template>

<style scoped>
</style>
