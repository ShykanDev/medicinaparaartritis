<template>
    <div class="">
        <header class="sticky top-0 z-50 w-full">
          <section>

          </section>
            <section class="w-full bg-white">
                <div class="flex w-full py-2 text-lg bg-white justify-evenly md:justify-center md:space-x-4 md:px-9 font-josefin-sans">
                    <RouterLink :class="{'border-b-orange-500 border-b-2 ': route.name === 'home'}" :to="{ name: 'home' }" >Inicio</RouterLink>
                    <RouterLink :class="{'border-b-orange-500 border-b-2': route.name === 'spaOne'}" :to="{ name: 'spaOne' }" >Beneficios</RouterLink>
                    <RouterLink :class="{'border-b-orange-500 border-b-2': route.name === 'spaTwo'}" :to="{ name: 'spaTwo' }" >Ingredientes</RouterLink>
                    <RouterLink :class="{'border-b-orange-500 border-b-2': route.name === 'spaThree'}" :to="{ name: 'spaThree' }" >Preguntas</RouterLink>
                    <!-- <RouterLink :class="{'border-b-orange-500 border-b-2': route.name === 'non'}" :to="{ name: 'home' }" >Prasadam</RouterLink> -->
                    <a class="hidden md:block" href="https://www.prasadam.mx/" target="_blank">Prasadam</a>
                </div>
                <div class="flex flex-col items-center justify-between px-4 py-2 text-sm text-white bg-orange-400 shadow-md md:flex-row md:text-xl font-poppins">
  <!-- Sección de enlaces de contacto -->
  <div class="flex flex-wrap items-center justify-center gap-4 md:justify-start">
    <a href="tel:+525563950178" class="flex items-center gap-2 hover:underline">
      <i class="fas fa-phone"></i>
      <span>+52 55 6395 0178</span>
    </a>
    <a href="tel:+525563950179" class="flex items-center gap-2 hover:underline">
      <i class="fas fa-phone"></i>
      <span>+52 55 6395 0179</span>
    </a>
    <a href="mailto:informes@prasadam.mx" class="flex items-center gap-2 hover:underline">
      <i class="fas fa-envelope"></i>
      <span>informes@prasadam.mx</span>
    </a>
    <a href="https://wa.me/525562516687" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2 hover:underline">
      <i class="fab fa-whatsapp"></i>
      <span>+52 5562516687</span>
    </a>
  </div>

  <!-- Sección del dominio y las imágenes (visible solo en pantallas md o mayores) -->
  <div class="items-center hidden gap-4 md:flex animate-fade-up animate-delay-300">
    <img class="w-8 md:w-12" src="../assets/ssl-certificate.png" alt="SSL Certificate">
    <p class="font-parkinsans">
  <span class="text-gray-900">medicina</span>
  <span class="text-teal-700">para</span>
  <span class="text-white">artritis</span>
  <span class="text-purple-700">.com</span>
</p>



    <img class="w-8 md:w-12" src="https://medicinaparaansiedad.com/img/logo.png" alt="Logo Medicina para Ansiedad">
  </div>
</div>


            </section>
        </header>
        <main class="overflow-hidden">
            <slot name="main">

            </slot>
        </main>
        <footer class="relative w-full p-6 text-white bg-orange-800 font-poppins">
  <!-- Sección Título -->
  <div class="mb-6 text-center">
    <h2 class="text-4xl font-bold lg:text-5xl">Contáctanos</h2>
  </div>

  <!-- Dirección -->
  <div class="flex flex-col items-center justify-between mb-6 md:flex-row">
    <div class="flex items-center gap-2 mb-4 md:mb-0">
      <i class="text-3xl fas fa-map-marker-alt lg:text-4xl"></i>
      <a href="https://www.google.com.mx/maps/place/Gutenberg+128,+Anzures,+Miguel+Hidalgo,+11590+Ciudad+de+México,+CDMX" target="_blank" rel="noopener noreferrer" class="text-sm font-bold lg:text-lg hover:underline">
        Gutenberg #128 Anzures, Miguel Hidalgo, 11590 Ciudad de México
      </a>
    </div>
    <iframe class="w-full h-48 lg:h-72 md:w-[60%] lg:w-[50%]" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3762.5395970522604!2d-99.1760704!3d19.4322888!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85d1f8b32758939b%3A0xf34fbd07bc47d6dd!2sGutenberg%20128%2C%20Anzures%2C%20Miguel%20Hidalgo%2C%2011590%20Ciudad%20de%20M%C3%A9xico%2C%20CDMX!5e0!3m2!1sen!2smx!4v1730328617197!5m2!1sen!2smx" allowfullscreen="false" loading="lazy" referrerpolicy="no-referrer-when-downgrade" style="border: 0;"></iframe>
  </div>

  <!-- Sección de Contactos -->
  <div class="grid grid-cols-1 gap-8 mb-8 text-center sm:grid-cols-2 lg:grid-cols-4">
    <!-- Teléfonos -->
    <div class="flex flex-col items-center">
      <i class="mb-2 text-3xl fas fa-phone"></i>
      <a href="tel:+525563950178" class="text-sm font-bold lg:text-lg hover:text-orange-500">
        +52 55 6395 0178
      </a>
    </div>
    <div class="flex flex-col items-center">
      <i class="mb-2 text-3xl fas fa-phone"></i>
      <a href="tel:+525563950179" class="text-sm font-bold lg:text-lg hover:text-orange-500">
        +52 55 6395 0179
      </a>
    </div>

    <!-- Email -->
    <div class="flex flex-col items-center">
      <i class="mb-2 text-3xl fas fa-envelope"></i>
      <a href="mailto:informes@prasadam.mx" class="text-sm font-bold lg:text-lg hover:text-orange-500">
        informes@prasadam.mx
      </a>
    </div>

    <!-- WhatsApp -->
    <div class="flex flex-col items-center">
      <i class="mb-2 text-3xl fab fa-whatsapp"></i>
      <a href="https://wa.me/525562516687" target="_blank" rel="noopener noreferrer" class="text-sm font-bold lg:text-lg hover:text-orange-500">
        +52 5562516687
      </a>
    </div>
  </div>

  <!-- Pie de página -->
  <div class="pt-4 mt-6 text-center border-t border-white">
    <p class="mb-2 text-sm font-bold lg:text-lg">
      Todos los derechos reservados &copy; {{new Date().getFullYear()}}
    </p>
    <p class="text-sm lg:text-lg">
      Design by <strong>PACA</strong>
    </p>
  </div>
</footer>



    </div>
</template>

<script lang="ts" setup>
// import IntroCard from '@/components/IntroCard.vue';
import { useRoute } from 'vue-router';

const route = useRoute();
</script>

<style scoped>

</style>
