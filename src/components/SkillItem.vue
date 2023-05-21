<template>
  <div class="skill">
    <span class="--label" :class="labelClass">{{label}} <span v-if="!subtitle" class="--percentage-indicator">({{ percentage }} %)</span> </span>
    <span class="--label-subtitle">{{ subtitle }}</span>
    <div class="--percentage-wrapper">
      <span class="--percentage-bar-empty" ></span>
      <span ref="percentageIndicator" class="--percentage-bar" ></span>
    </div>
  </div>
</template>
<script setup lang="ts">
import { onMounted, onUpdated, ref } from 'vue';

const props = defineProps<{
  label: string,
  subtitle?: string,
  percentage: number,
  labelClass?: string,
  percentageBarClass?: string,

}>()

const percentageIndicator = ref<HTMLSpanElement>()
const handleViewChanges = () => {
  if(percentageIndicator.value != undefined)
    percentageIndicator.value!.style.width =  props.percentage + "%"
}

onUpdated(() => {
  handleViewChanges()
})

onMounted(() => {
  handleViewChanges()
})

</script>
<style lang="scss">
.skill{
  display: flex;
  flex-direction: column;
  .--label{
    letter-spacing: 1px;
    font-size: 0.9rem;
    font-weight: 600;
    text-transform: uppercase;
  }
  &>.--percentage-wrapper{
    margin-top: 0.8rem;
    position: relative;
    display: flex;
    flex-direction: column;
    border-radius: 0.5rem;
    overflow: hidden;
    .--percentage-bar-empty{
      
      height: 0.5rem;
      background-color: var(--on-surface-transparent-color);
      
    }
    .--percentage-bar{
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      background-color: var(--primary-color);
      border-radius: inherit;
    }
  }
}
</style>