<script setup lang="ts">
import Divider from 'primevue/divider'

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
            <a
              class="bg-linear-to-t from-yellow-200 from-0% to-yellow-200 to-100% font-medium text-[#3f3f6d] no-underline transition-[background-size] duration-200 [background-size:100%_42%] [background-position:0_100%] [background-repeat:no-repeat] hover:[background-size:100%_100%]"
              :href="profile.github"
              target="_blank"
              rel="noopener"
            >
              GitHub </a
            >.
          </p>

          <p>
            For contact, send me an
            <a
              class="bg-linear-to-t from-yellow-200 from-0% to-yellow-200 to-100% font-medium text-[#3f3f6d] no-underline transition-[background-size] duration-200 [background-size:100%_42%] [background-position:0_100%] [background-repeat:no-repeat] hover:[background-size:100%_100%]"
              :href="`mailto:${profile.email}`"
            >
              email
            </a>
            or reach me on
            <a
              class="bg-linear-to-t from-yellow-200 from-0% to-yellow-200 to-100% font-medium text-[#3f3f6d] no-underline transition-[background-size] duration-200 [background-size:100%_42%] [background-position:0_100%] [background-repeat:no-repeat] hover:[background-size:100%_100%]"
              :href="profile.linkedin"
              target="_blank"
              rel="noopener"
            >
              LinkedIn </a
            >.
          </p>
        </div>

        <p class="mt-6 max-w-xl text-sm leading-6 text-[#3f3f6d]/60">{{ technologySummary }}</p>
      </section>

      <aside
        class="w-full max-w-[23rem] min-w-0 justify-self-center text-sm leading-6 text-[#3f3f6d]/80"
        aria-label="Experience and project links"
      >
        <div>
          <h2 class="text-base font-semibold text-[#3f3f6d]">Experience</h2>
          <Divider class="my-3" />

          <div class="space-y-4">
            <article v-for="item in experience" :key="item.title">
              <p class="font-medium text-[#3f3f6d]">{{ item.title }}</p>
              <p>{{ item.organization }}</p>
              <time class="text-xs font-medium uppercase text-[#3f3f6d]/60">{{ item.period }}</time>
            </article>
          </div>
        </div>

        <div class="mt-8">
          <h2 class="text-base font-semibold text-[#3f3f6d]">Projects</h2>
          <Divider class="my-3" />

          <div class="space-y-4">
            <article v-for="project in projects" :key="project.name">
              <a
                class="bg-linear-to-t from-yellow-200 from-0% to-yellow-200 to-100% font-medium text-[#3f3f6d] no-underline transition-[background-size] duration-200 [background-size:100%_42%] [background-position:0_100%] [background-repeat:no-repeat] hover:[background-size:100%_100%]"
                :href="project.link"
                target="_blank"
                rel="noopener"
              >
                {{ project.name }}
              </a>
              <p>{{ project.detail }}</p>
            </article>
          </div>
        </div>
      </aside>
    </div>
  </main>
</template>
