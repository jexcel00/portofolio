<template>
  <button @click="onSwitchTheme" class="theme-switcher">
    <span class="material-icons">
      {{ themeIcon }}
    </span>
  </button>
</template>
<script setup lang="ts">
import { computed, ref } from 'vue'
const theme = ref(document.body.getAttribute('data-theme') ?? 'light')

const themeIcon = computed(() => {
  return theme.value == 'light' ? 'light_mode' : 'dark_mode'
})

const onSwitchTheme = () => {
  theme.value = theme.value == 'light' ? 'dark' : 'light'
  document.body.setAttribute('data-theme', theme.value)
}
</script>
<style lang="scss">
.theme-switcher{
  position: fixed;
  left: 2rem;
  bottom: 2rem;
  width: 55px;
  height: 55px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  //box-shadow: -1px 49px 54px -25px rgba(0,0,0,0.69);
  box-shadow: 0 5px 8px rgba($color: #000000, $alpha: 0.25)
  //-moz-box-shadow: -1px 49px 54px -25px rgba(0,0,0,0.69);
  
}
</style>