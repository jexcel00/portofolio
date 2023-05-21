<template>
  <div>
    <NavBar></NavBar>
    <HeroSection></HeroSection>
    <AboutSection></AboutSection>
    <SkillsSection></SkillsSection>
    <CareerSection></CareerSection>
    <RealizationSection></RealizationSection>
  </div>
  <ThemeSwitcher class="bg-primary text-on-primary"/>
</template>
<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import HeroSection from './components/HeroSection.vue';
import ThemeSwitcher from './components/generics/ThemeSwitcher.vue';
import AboutSection from './components/AboutSection.vue';
import SkillsSection from './components/SkillsSection.vue';
import CareerSection from './components/CareerSection.vue';
import RealizationSection from "./components/RealizationSection.vue"


</script>