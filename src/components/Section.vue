<script setup>
defineProps({
  id: { type: String, required: true },
  bg: { type: String, default: null },
});
</script>

<template>
  <section :id="id" class="relative h-screen w-screen snap-start flex flex-col overflow-hidden shrink-0">
    <img v-if="bg" :src="bg" alt="" class="absolute inset-0 w-full h-full object-cover -z-10" />
    <slot />
  </section>
</template>

<style scoped>
section :is(h1, h2) {
  text-transform: uppercase;
  margin-top: 5rem;
}
</style>
