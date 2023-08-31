<script setup>
import { onBeforeMount } from 'vue';
import { RouterLink } from 'vue-router';


// rappel: onBeforeMount est appelé automatiquement quand le composant est "mount", chargé
// comme la navigation n'est plus gêrée par le navigateur mais intercepté par vue, on remarque que ce composant de Nav
// n'est chargé qu'une seule fois: à l'initialisation
onBeforeMount(()=>{
  console.log('%c TheNav:: onBeforeMount()', 'background-color:white;color:blue;');
})

</script>


<template>
  <nav id="header" class="w-full z-30 top-0 bg-gradient-to-r from-emerald-400 to-cyan-400">
        <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
          <div class="pl-4 flex items-center">         
            <router-link :to="{name:'home'}" class="no-underline hover:no-underline font-bold text-2xl lg:text-4xl">VUE ROUTER</router-link>
          </div>
          <div class="block lg:hidden pr-4">
            <button id="nav-toggle" class="flex items-center p-1 text-pink-800 hover:text-gray-900 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out">
              <svg class="fill-current h-6 w-6" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                <title>Menu</title>
                <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
              </svg>
            </button>
          </div>
          <div class="w-full flex-grow lg:flex lg:items-center lg:w-auto hidden mt-2 lg:mt-0 text-black p-4 lg:p-0 z-20" id="nav-content">
            <ul class="list-reset lg:flex justify-end flex-1 items-center">
              <li class="mr-3">
                <RouterLink to="/" class="inline-block py-2 px-4 text-black font-bold no-underline">Home</RouterLink>
              </li>
              <li class="mr-3">
                <RouterLink to="/products" class="inline-block text-black no-underline hover:text-gray-800 hover:text-underline py-2 px-4">Products</RouterLink>
                <!-- <a class="inline-block text-black no-underline hover:text-gray-800 hover:text-underline py-2 px-4" href="#">Products</a> -->
              </li>
            </ul>
          </div>
        </div>
        <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
    </nav>
</template>



<style scoped>



.router-link-exact-active{
  border-bottom: 2px dotted rgb(223, 224, 223);
}



</style>