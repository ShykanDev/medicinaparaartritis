<template>
  <div
    class="max-w-lg mx-auto overflow-hidden bg-white border rounded-lg shadow-md border-green-50 md:max-w-lg "
  >
    <!-- Imagen -->
    <img :src="image" alt="Card image" class="object-cover w-full max-h-60 " />

    <!-- Contenido -->
    <div class="p-4">
      <!-- Título -->
      <h2 class="mb-2 text-xl font-semibold text-center text-orange-600 border-b-2 border-b-orange-500 font-poppins ">{{ title }}</h2>

      <!-- Resumen -->
      <p class="text-base text-gray-600 font-poppins" v-html="highlightedText(summary)"></p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

// Definimos las props con valores predeterminados
defineProps({
  title: {
    type: String,
    default: 'Título de ejemplo',
  },
  summary: {
    type: String,
    default: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla eget massa nec nunc pretium consequat.',
  },
  image: {
    type: String,
    default: 'https://storage.googleapis.com/a1aa/image/MWJSpm8Ynar9AF9kA7luRMNBDgJW7uTpccNt2dHQLEG1oU9E.jpg',
  },
});

const highlightedText  = (text: string) => {
  return text.replace(/\b(estrés)\b/gi,'<span class="font-bold text-orange-600">Estrés</span>')
  .replace(/\b(prevenir el desgaste)\b/gi,'<span class="font-bold text-orange-600">PREVENIR EL DESGASTE</span>')
  .replace(/\b(Fortalece)\b/gi,'<span class="font-bold text-orange-600">FORTALECE</span>')
  .replace(/\b(estrés)\b/gi,'<span class="font-bold text-orange-600">ESTRÉS</span>')
  .replace(/\b(proteger)\b/gi,'<span class="font-bold text-orange-600">PROTEGER</span>')
  .replace(/\b(alivio)\b/gi,'<span class="font-bold text-orange-600">ALIVIO</span>')
  .replace(/\b(reducir la inflamación)\b/gi,'<span class="font-bold text-orange-600">REDUCIR LA INFLAMACIÓN</span>')
  .replace(/\b(segura y efectiva)\b/gi,'<span class="font-bold text-orange-600">SEGURA Y EFECTIVA</span>')
  .replace(/\b(flexibilidad)\b/gi,'<span class="font-bold text-orange-600">FLEXIBILIDAD</span>')
  .replace(/\b(articulaciones)\b/gi,'<span class="font-bold text-orange-600">ARTICULACIONES</span>')
  .replace(/\b(rigidez)\b/gi,'<span class="font-bold text-orange-600">RIGIDEZ</span>')
  .replace(/\b(equilibra)\b/gi,'<span class="font-bold text-orange-600">EQUILIBRA</span>')
  .replace(/\b(huesos)\b/gi,'<span class="font-bold text-orange-600">HUESOS</span>')
  .replace(/\b(músculos)\b/gi,'<span class="font-bold text-orange-600">MÚSCULOS</span>')
  .replace(/\b(absorción)\b/gi,'<span class="font-bold text-orange-600">ABSORCIÓN</span>')
  .replace(/\b(inmunológico)\b/gi,'<span class="font-bold text-orange-600">INMUNOLÓGICO</span>')
  .replace(/\b(óseo)\b/gi,'<span class="font-bold text-orange-600">ÓSEO</span>')
  .replace(/\b(recuperación)\b/gi,'<span class="font-bold text-orange-600">RECUPERACIÓN</span>')
  .replace(/\b(reduce)\b/gi,'<span class="font-bold text-orange-600">REDUCE</span>')
  .replace(/\b(estimula)\b/gi,'<span class="font-bold text-orange-600">ESTIMULA</span>')
  .replace(/\b(reparación)\b/gi,'<span class="font-bold text-orange-600">REPARACIÓN</span>')
  .replace(/\b(beneficios)\b/gi,'<span class="font-bold text-orange-600">BENEFICIOS</span>')
  .replace(/\b(equilibrar)\b/gi,'<span class="font-bold text-orange-600">EQUILIBRAR</span>')
  .replace(/\b(fortalecer)\b/gi,'<span class="font-bold text-orange-600">FORTALECER</span>')
  .replace(/\b(inflamación)\b/gi,'<span class="font-bold text-orange-600">INFLAMACIÓN</span>')
}
</script>

<style>
/* No es necesario agregar estilos personalizados debido a TailwindCSS */
</style>
