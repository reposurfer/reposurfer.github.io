<script setup lang="ts">
import HomeIntro from '@/components/home/HomeIntro.vue'
import HomeSidebar from '@/components/home/HomeSidebar.vue'

const profile = {
  name: 'Stef',
  role: 'Software Developer',
  summary:
    'I build practical web applications with clean interfaces, reliable structure, and a focus on shipping useful things.',
  email: 'hello@example.com',
  github: 'https://github.com/reposurfer',
  linkedin: 'https://www.linkedin.com/',
}

const experience = [
  {
    period: '2024 - Present',
    title: 'Software Developer',
    organization: 'Current Role or Company',
  },
  {
    period: '2023 - 2024',
    title: 'Developer Experience',
    organization: 'Company or Organization',
  },
  {
    period: 'Earlier',
    title: 'Technical Training',
    organization: 'Program, certification, or self-directed work',
  },
]

const projects = [
  {
    name: 'Portfolio Website',
    detail: 'Vue, Tailwind CSS, PrimeVue',
    link: 'https://reposurfer.github.io/',
  },
  {
    name: 'Project Name',
    detail: 'Web app or tool',
    link: 'https://github.com/reposurfer',
  },
  {
    name: 'Another Project',
    detail: 'Automation, dashboard, or prototype',
    link: 'https://github.com/reposurfer',
  },
]

const technologySummary =
  'I am currently proficient with Vue, TypeScript, C#, .NET, Entity Framework, SQL, and Azure, while continuing to learn more and broaden the tools I can use well.'
</script>

<template>
  <main
    class="fixed inset-0 overflow-hidden bg-[#fbfaf7] font-['Instrument_Sans',sans-serif] font-normal text-[#3f3f6d] [font-optical-sizing:auto] [font-style:normal] [font-variation-settings:'wdth'_100]"
  >
    <div
      class="grid h-full w-full content-start gap-8 px-6 pt-[14vh] sm:px-10 md:grid-cols-[minmax(0,36rem)_1fr] lg:ml-[7vw] lg:pr-[7vw] xl:ml-[8vw] xl:pr-[8vw]"
    >
      <HomeIntro :profile="profile" :technology-summary="technologySummary" />
      <HomeSidebar :experience="experience" :projects="projects" />
    </div>
  </main>
</template>
