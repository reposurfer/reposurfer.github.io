<script setup lang="ts">
import HomeHighlightLink from './HomeHighlightLink.vue'

export type ProjectItem = {
  name: string
  detail: string
  link: string
}

defineProps<{
  projects: ProjectItem[]
}>()
</script>

<template>
  <div class="space-y-4">
    <article v-for="project in projects" :key="project.name">
      <HomeHighlightLink :href="project.link" external>
        {{ project.name }}
      </HomeHighlightLink>
      <p>{{ project.detail }}</p>
    </article>
  </div>
</template>
