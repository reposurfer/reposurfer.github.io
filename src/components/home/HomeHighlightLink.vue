<script setup lang="ts">
defineProps<{
  href: string
  external?: boolean
}>()
</script>

<template>
  <a
    class="bg-linear-to-t from-yellow-200 from-0% to-yellow-200 to-100% font-medium text-[#3f3f6d] no-underline transition-[background-size] duration-200 [background-size:100%_42%] [background-position:0_100%] [background-repeat:no-repeat] hover:[background-size:100%_100%]"
    :href="href"
    :target="external ? '_blank' : undefined"
    :rel="external ? 'noopener' : undefined"
  >
    <slot />
  </a>
</template>
