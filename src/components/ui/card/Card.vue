<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { cn } from '@/lib/utils'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <div class="card-container"
    :class="
      cn(
        'rounded-xl text-card-foreground',
        props.class,
      )
    "
  >
    <slot />
  </div>
</template>

<style scoped>
.card-container {
  max-height: 600px;
  overflow-y: auto;
  box-sizing: border-box;
}

.card-container::-webkit-scrollbar {
  width: 3px;

}

.card-container::-webkit-scrollbar-thumb {
  background-color: #929292;
  border-radius: 1px;
}

@media (max-width: 800px) {
  .card-container {
    max-height: 580px;
  }
}
@media (max-width: 500px) {
  .card-container {
    max-height: 560px;
  }
}


</style>
