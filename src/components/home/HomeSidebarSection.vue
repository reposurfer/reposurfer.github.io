<script setup lang="ts">
import Divider from 'primevue/divider'

defineProps<{
  title: string
}>()
</script>

<template>
  <section>
    <h2 class="text-base font-semibold text-[#3f3f6d]">{{ title }}</h2>
    <Divider class="my-3" />

    <slot />
  </section>
</template>
