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
        'rounded-xl border text-card-foreground shadow',
        props.class,
      )
    "
  >
    <slot />
  </div>
</template>

<style scoped>
.card-container {
  max-height: 500px;
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

</style>
