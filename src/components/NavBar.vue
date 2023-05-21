<template>
  <nav class="flex items-center justify-between px-8 py-3 border-b border-gray-200">
    <h1 class="text-lg font-bold">Portfolio</h1>
    <ul class="flex items-center gap-7">
      <li v-for="link in links" :key="link.href">
        <a @click="hash = link.href" :class="{'text-primary font-semibold': link.href == hash}" :href="link.href">{{ link.label }}</a>
       
      </li>
      <li class="flex px-4 py-3 text-sm font-medium rounded-lg bg-primary text-on-primary">
        <a href="#/">Me contacter</a>
      </li>
       
    </ul>
   
  </nav>
</template>
<script lang="ts" setup>
import { ref } from 'vue';
import { useRoute } from 'vue-router';

const hash = ref("#")

const links = ref([
  {
    label: "Accueil",
    href: "#"
  },
  {
    label: "A propos",
    href: "#about_me"
  },
  {
    label: "Mes compétences",
    href: "#skills"
  },
  {
    label: "Mes réalisations",
    href: "#realizations"
  }
])
</script>