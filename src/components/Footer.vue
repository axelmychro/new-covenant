<script setup>
import { ref } from "vue";

const characterName = ref("Exusiai");
const companyName = ref("HYPERGRYPH");
</script>

<template>
  <footer class="fixed w-full bottom-0 left-0 bg-transparent text-white">
    <div class="text-8xl m-8">
      <p>{{ characterName }}</p>
    </div>
    <div class="border-t border-white">
      <div class="text-xl m-8">
        <small>
          &copy; <span class="font-aboreto">{{ companyName }}</span>
        </small>
      </div>
    </div>
  </footer>
</template>

<style scoped>
/* Add any additional styles if needed */
</style>
