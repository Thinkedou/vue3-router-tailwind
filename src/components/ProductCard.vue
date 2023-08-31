<script setup>
import { onBeforeMount } from 'vue';


onBeforeMount(()=>{
  console.log('%c ProductCard:: onBeforeMount()', 'background-color:lime;color:grey;');
})
</script>


<template>
  <div class="max-w-sm rounded overflow-hidden shadow border-solid border-2 border-emerald-200">
      <img class="w-full" src="https://tailwindui.com/img/ecommerce-images/product-feature-03-detail-02.jpg" alt="Sunset in the mountains">
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">The walnut wood</div>
        <p class="text-gray-700 text-base">
          The powder coated steel divider separates active cards from new ones, or can be used to archive important task lists        </p>
      </div>
      <div class="px-6 pt-4 pb-2">
        <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#photography</span>
        <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#wood</span>
        <span class="inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2 mb-2">#bs</span>
      </div>
    </div>
</template>



<style lang="scss" scoped>
</style>