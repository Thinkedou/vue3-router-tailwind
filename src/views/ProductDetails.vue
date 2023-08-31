<script  setup>
import {ref, onBeforeMount} from "vue"
import { useRoute } from 'vue-router'
import ProductCard from '../components/ProductCard.vue';

const route = useRoute()
const productId = ref(0)

const catchProductId = ()=>{
  console.log(route)
  productId.value = route.params.productId
}

catchProductId()


onBeforeMount(()=>{
  console.log('%c ProductDetails:: onBeforeMount()', 'background-color:blue;color:white;');
})





</script>

<template>
  <div class="mx-auto max-w-2xl py-24 flex">
    <h2 class="text-3xl font-bold mx-12"> Product ID: {{ route.params.productId }} </h2>
    <ProductCard />

  </div>
</template>
