<script setup lang="ts">
import HomeHighlightLink from './HomeHighlightLink.vue'

type Profile = {
  name: string
  role: string
  summary: string
  email: string
  github: string
  linkedin: string
}

defineProps<{
  profile: Profile
  technologySummary: string
}>()
</script>

<template>
  <section class="min-w-0 max-w-xl" aria-labelledby="intro-title">
    <h1
      id="intro-title"
      class="text-[clamp(3rem,7vw,4.75rem)] font-bold leading-none tracking-normal"
    >
      {{ profile.name }}
    </h1>

    <div class="mt-5 max-w-xl space-y-4 text-base leading-7 text-[#3f3f6d]/80">
      <p>
        I am a
        <span class="font-medium text-[#3f3f6d]">{{ profile.role }}</span>
        focused on building practical software for the web.
        {{ profile.summary }}
      </p>

      <p>
        Most of my work sits around frontend development, typed JavaScript, and small tools that
        make everyday workflows cleaner. You can find public work on
        <HomeHighlightLink :href="profile.github" external>GitHub</HomeHighlightLink>.
      </p>

      <p>
        For contact, send me an
        <HomeHighlightLink :href="`mailto:${profile.email}`">email</HomeHighlightLink>
        or reach me on
        <HomeHighlightLink :href="profile.linkedin" external>LinkedIn</HomeHighlightLink>.
      </p>
    </div>

    <p class="mt-6 max-w-xl text-sm leading-6 text-[#3f3f6d]/60">{{ technologySummary }}</p>
  </section>
</template>
