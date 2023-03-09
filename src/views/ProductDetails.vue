<script  setup>
import {ref} from "vue"
import { useRoute } from 'vue-router'
import ProductCard from '../components/ProductCard.vue';

const route = useRoute()
const productId = ref(0)

const catchProductId = ()=>{
  productId.value = route.params.id
}

catchProductId()

</script>

<template>
  <div class="mx-auto max-w-2xl py-24 flex">
    <h2 class="text-3xl font-bold mx-12"> Product ID: {{ productId }} </h2>
    <ProductCard />

  </div>
</template>
