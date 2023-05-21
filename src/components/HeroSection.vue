<template>
  <div class="flex justify-center">
    <div class="flex flex-col-reverse lg:grid items-center justify-center lg:grid-cols-2 gap-20 my-44 lg:w-[1000px]">
      <div class="flex justify-end">
        <HeroPresentation class="self-end w-[450px]"></HeroPresentation>
      </div>
      <HeroAvatar class="md:self-start"></HeroAvatar>
    </div>
  </div>
</template>
<script lang="ts" setup>
import HeroPresentation from './HeroPresentation.vue';
import HeroAvatar from './HeroAvatar.vue';
</script>