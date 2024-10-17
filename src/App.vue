<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'

const abrirMenuHamburguer = ref(false);

</script>

<template>
  <header class="bg-gray-800 border-b-2 border-gray-900 sticky top-0 hidden">
      <nav class="flex flex-row justify-between">
        <div class="flex flex-row justify-between items-center w-[90%] mx-auto">
          <div>
              <img class="w-16 cursor-pointer" src="/public/Img/logo2.png" alt="...">
          </div>
          <div class="bg-red-600">
          </div>
          <div class="w-full">
            <div class="text-white duration-500 bg-gray-800 md:min-h-[8vh] left-0 md:w-auto w-full flex justify-end items-center">
              <ul class="sm:flex md:flex-row md:items-center hidden justify-end md:gap-[4vw] gap-8">
                  <li>
                      <a class="hover:text-gray-500" href="#">Inicio</a>
                  </li>
                  <li>
                      <a class="hover:text-gray-500" href="#">Solution</a>
                  </li>
                  <li>
                      <a class="hover:text-gray-500" href="#">Resource</a>
                  </li>
                  <li>
                      <a class="hover:text-gray-500" href="#">Contacto</a>
                  </li>
              </ul>
            </div>
          </div>
          <div class="flex items-center gap-6 text-white">
              <ion-icon @click="abrirMenuHamburguer" name="menu" class="text-3xl cursor-pointer sm:hidden"></ion-icon>
          </div>
        </div>
      </nav>
  </header>
  <div id="inicio">
    <HelloWorld />
  </div>
</template>