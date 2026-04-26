<script setup lang="ts">
import HomeExperienceList, { type ExperienceItem } from './HomeExperienceList.vue'
import HomeProjectList, { type ProjectItem } from './HomeProjectList.vue'
import HomeSidebarSection from './HomeSidebarSection.vue'

defineProps<{
  experience: ExperienceItem[]
  projects: ProjectItem[]
}>()
</script>

<template>
  <aside
    class="w-full max-w-[23rem] min-w-0 justify-self-center text-sm leading-6 text-[#3f3f6d]/80"
    aria-label="Experience and project links"
  >
    <HomeSidebarSection title="Experience">
      <HomeExperienceList :items="experience" />
    </HomeSidebarSection>

    <HomeSidebarSection class="mt-8" title="Projects">
      <HomeProjectList :projects="projects" />
    </HomeSidebarSection>
  </aside>
</template>
