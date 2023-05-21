<template>
  <section id="skills" class="px-4 py-12">
    <h2 class="mb-16 text-xl font-bold text-center uppercase opacity-80" style="letter-spacing: 8px;">Mes compétences</h2>
    <div class="flex justify-center class">
      <div class="lg:w-[1000px]">
        <h3 class="mb-8 text-xl font-light uppercase" style="letter-spacing: 0.5rem;">Techniques</h3>
        <div class="grid grid-cols-2 gap-12 lg:grid-cols-3">
          <SkillItem :key="skill.label" v-for="skill in techSkills" :label="skill.label" :percentage="skill.percentage" percentage-bar-class="" label-class="" />
        </div>
        <div class="my-20 app-divider"></div>

        <h3 class="mb-8 text-xl font-light uppercase" style="letter-spacing: 0.5rem;">Linguistiques</h3>
        <div class="grid grid-cols-2 gap-12 lg:grid-cols-3">
          <SkillItem :key="skill.label" v-for="skill in linguisticSkills" :subtitle="skill.subtitle" :label="skill.label" :percentage="skill.percentage" percentage-bar-class="" label-class="" />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts">
import { ref } from 'vue';
import SkillItem from './SkillItem.vue';
 const techSkills = ref([
  {
    label: "C++",
    percentage: 40
  },
  {
    label: "C",
    percentage: 40
  },
  {
    label: "PHP",
    percentage: 55
  },
  {
    label: "C#",
    percentage: 25
  },
  {
    label: "JAVA",
    percentage: 55
  },
  {
    label: "SQL",
    percentage: 60
  },
  {
    label: "Trello",
    percentage: 75
  },
  {
    label: "Bootstrap",
    percentage: 75
  },
  {
    label: "Wordpress",
    percentage: 75
  },
  {
    label: "HTML",
    percentage: 40
  },
  {
    label: "CSS",
    percentage: 40
  }
 ])

 const linguisticSkills = ref([
  {
    label: "Français",
    percentage: 100,
    subtitle: "Langue maternelle"
  },
  {
    label: "Anglais",
    percentage: 75,
    subtitle: "Niveau C1"
  },
  {
    label: "Espagnol",
    percentage: 80,
    subtitle: "Niveau C1-C2"
  }
 ])

</script>