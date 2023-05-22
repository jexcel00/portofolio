<template>
  <nav class="flex items-center justify-between px-8 py-3 border-b border-gray-200">
    <h1 class="text-lg font-bold">Portfolio</h1>
    <button @click="onToggleButtonClicked" class="flex items-center justify-center p-2 text-black rounded-full bg-slate-100 lg:hidden"><span class="material-icons">menu</span></button>
    <div ref="linksParentRef" class="fixed top-0 bottom-0 left-0 z-50 hidden p-4 bg-surface shadow-lg lg:block lg:relative lg:w-auto w-[350px] lg:p-0 lg:shadow-none">
      <ul  class="flex flex-col items-center gap-8 lg:flex-row">
      <li v-for="link in links" :key="link.href">
        <a @click="onLinkClicked(link.href)" :class="{'text-primary font-semibold': link.href == hash}" :href="link.href">{{ link.label }}</a>
       
      </li>
      <li class="flex px-4 py-3 text-sm font-medium rounded-lg bg-primary text-on-primary">
        <a href="#contact">Me contacter</a>
      </li>
       
    </ul>
    </div>
   
  </nav>
</template>
<script lang="ts" setup>
import { ref } from 'vue';


const hash = ref("#")

const linksParentRef = ref<HTMLElement | null>(null)

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

const onLinkClicked = (href: string) => {
  hash.value = href;
  linksParentRef.value?.classList.toggle('hidden')
  
}
const onToggleButtonClicked = () => {

  linksParentRef.value?.classList.toggle('hidden')
  
}
</script>