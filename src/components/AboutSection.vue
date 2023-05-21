<template>
  <section id="about_me" class="px-4 py-12 bg-primary text-on-primary">
    <h2 class="mb-16 text-xl font-bold text-center uppercase opacity-80" style="letter-spacing: 8px;">A propos</h2>
    <div class="flex flex-col-reverse items-center gap-20 my-4 ms-center jus lg:grid-cols-2 lg:grid ">
      <div class="flex lg:justify-end">
        <AboutImage></AboutImage>
      </div>
      <AboutDescription class="h-full lg:self-start"></AboutDescription>
    </div>
  </section>
</template>
<script lang="ts" setup>
import AboutDescription from './AboutDescription.vue';
import AboutImage from './AboutImage.vue';

</script>