<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { cn } from '@/lib/utils'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()
</script>

<template>
  <div :class="cn(' p-6 pt-0', props.class)" 
  style="font-family: 'e-Ukraine-Thin', sans-serif; color: #c2c2c2; font-size: 13px; max-height: 500px;">
    <slot />
  </div>
</template>

