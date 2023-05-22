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
            <a target="_blank" v-if="realization.link" :href="realization.link" class="self-start px-8 py-3 mt-8 rounded-full bg-primary text-on-primary">Voir plus</a>
          </div>
          <img class="shadow-lg" :class="{'col-start-1 row-start-1': index % 2 == 1 }" :src="realization.image" style="width: 100%; object-fit: cover; height: 400px;" alt="" srcset=""/>
          
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
    image: "/imgs/qr_code_scanning.png",
    description: `Durant ma première année de stage, afin d'améliorer mes compétences et me familiariser avec les langages html et css j'ai réalisé plusieurs mini-projet de façon indépendante sur le site https://www.frontendmentor.io/.`,
    link: "https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H"
  },
  {
    title: "Evolution des canaux digitaux",
    image: "/imgs/evo_canaux.jpg",
    description: "Durant ma deuxième année de stage il m'a été demandé de faire une étude sur l'évolution des canaux digitaux en Afrique et plus précisément au Cameroun.",
    link: "/assets/files/canaux_bancaire.pages"
  },

  {
    title: "Client lourd PPE",
    image: "/imgs/client_lourd.jpeg",
    description: "Ce projet est une application codé en Java avec la structure MVC qui permet de faire la gestion des élèves, moniteurs, formules",
    link: null
  },
  {
    title: "Calculatrice",
    image: "/imgs/calculatrice.jpeg",
    description: `création d'une calculatrice en Java à l'aide de la bibliothèque Swing.
    J'ai choisi de réaliser ce projet pour apprendre la bibliothèque Swing.
    Une compétences qui me sera indispensable par la suite.`,
    link: null
  },
  {
    title: "Convertisseur",
    image: "/imgs/convertisseur.jpeg",
    description: `Convertisseur de FCFA vers EURO et vice-versa. Réalisé avec la bibliothèque Java Swing`,
    link: null
  },
  
])
</script>