<script  setup>
import { useRouter } from 'vue-router'
import ProductCard from '../components/ProductCard.vue';

const router = useRouter()

const openOneProduct = (pId)=>{
  const routeParams = {
    name:'productDetails',
    params:{
      productId:pId
    }
  }
  // on "push" dans le tableau de navigation, ce qui provoque la redirection 
  router.push(routeParams)
}



</script>

<template>
  <div class="mx-auto max-w-2xl py-24 flex space-x-2">
    
    <ProductCard @click="openOneProduct(15)" />
    <ProductCard @click="openOneProduct(8)" />
    <ProductCard @click="openOneProduct(7)" />


  </div>
</template>
