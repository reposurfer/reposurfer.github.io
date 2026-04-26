<script setup lang="ts">
export type ExperienceItem = {
  period: string
  title: string
  organization: string
}

defineProps<{
  items: ExperienceItem[]
}>()
</script>

<template>
  <div class="space-y-4">
    <article v-for="item in items" :key="item.title">
      <p class="font-medium text-[#3f3f6d]">{{ item.title }}</p>
      <p>{{ item.organization }}</p>
      <time class="text-xs font-medium uppercase text-[#3f3f6d]/60">{{ item.period }}</time>
    </article>
  </div>
</template>
