<script setup>
defineProps({
  id: { type: String, required: true },
  bg: { type: String, default: null },
});
</script>

<template>
  <section :id="id" class="relative h-screen snap-start flex flex-col overflow-hidden">
    <img v-if="bg" :src="bg" alt="" class="absolute inset-0 w-full h-full object-cover -z-10" />
    <slot />
  </section>
</template>

<style>
section :is(h1, h2) {
  @apply uppercase mt-[5rem];
}
</style>
