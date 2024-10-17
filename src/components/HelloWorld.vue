<script setup>
import { onMounted, ref } from 'vue'
import Typewriter from 'typewriter-effect/dist/core'

const typewriter = ref(null)

onMounted(() => {
  new Typewriter(typewriter.value, {
    loop: true,    // Para que el efecto se repita
    delay: 75,     // Velocidad al escribir las letras
    deleteSpeed: 60 // Velocidad al borrar las letras
  })
    .typeString('Desarrollador Frontend')  // Escribe el texto
    .pauseFor(1500)  // Pausa antes de borrar
    .deleteAll()     // Borra todo el texto
    .pauseFor(1000)  // Pausa antes de volver a escribir
    .start()         // Inicia el bucle
})
</script>

<template>
  <div class="w-full flex flex-row justify-center items-center min-h-[calc(100vh-64px)] relative">
    <img class="w-full h-screen object-cover" src="/public/Img/fondo.jpg" alt="Logo"/>

    <div class="absolute inset-0 bg-black bg-opacity-50 backdrop-blur-sm z-5"></div>

    <div class="absolute inset-0 flex flex-col justify-center items-center text-white z-10 gap-y-2.5" data-aos="zoom-in-up">
      <h1 class="text-4xl font-bold">LEONARDO GARCIA JIMENEZ</h1>
      <div class="text-xl" ref="typewriter"></div>
      <h2 class="text-sm whitespace-break-spaces px-80">
        Soy un desarrollador especializado en la creación de soluciones tecnológicas para la optimización de procesos administrativos. Mi objetivo es proporcionar sistemas personalizados y escalables que respondan a las necesidades específicas de cada negocio, impulsando la transformación digital y facilitando la gestión integral de las organizaciones.
      </h2>
    </div>
  </div>
</template>


<style scoped>
.text-xl {
  font-size: 1.25rem; /* O ajusta según tus preferencias */
}
</style>
