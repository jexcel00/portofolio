<template>
  <section id="realizations" class="px-4 py-12">
    <h2 class="mb-16 text-xl font-bold text-center uppercase opacity-80" style="letter-spacing: 8px;">Mes réalisations</h2>
    <div class="flex justify-center class">
      <div class="lg:w-[1000px] flex flex-col gap-28">
        <div v-for="(realization, index) in realizations" :key="realization.title" class="grid grid-cols-1 gap-16 lg:grid-rows-1 lg:grid-cols-2 bg-red">
          <div class="flex flex-col" :class="{'lg:col-start-2': index % 2 == 1 }">
            <h2 class="mb-8 text-4xl font-bold">{{ realization.title }}</h2>
            <p class="text-xl text-slate-500">
              {{ realization.description }}
            </p>
            <a target="_blank" :href="realization.link" class="self-start px-8 py-3 mt-8 rounded-full bg-primary text-on-primary">Voir plus</a>
          </div>
          <img :class="{'col-start-1 row-start-1': index % 2 == 1 }" :src="realization.image" style="width: 100%; object-fit: cover; height: 400px;" alt="" srcset=""/>
          
        </div>

        
      </div>
    </div>
  </section>
</template>


<script setup lang="ts">
import { ref } from 'vue';

const realizations = ref([
  {
    title: "Création d'interfaces",
    image: "/src/assets/imgs/qr_code_scanning.png",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis quibusdam aliquam quam. Corporis provident, voluptatibus quod nobis non nemo inventore.",
    link: "https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H"
  },
  {
    title: "Evolution des canaux digitaux",
    image: "/src/assets/imgs/evo_canaux.jpg",
    description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis quibusdam aliquam quam. Corporis provident, voluptatibus quod nobis non nemo inventore.",
    link: "/src/assets/files/canaux_bancaire.pages"
  }
])
</script>