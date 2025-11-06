<script setup>
import { Share2, AudioLines, User, Menu } from "lucide-vue-next";
</script>

<template>
  <header>
    <div class="bg-black/50 z-50 uppercase fixed top-0 left-0 w-full h-20 flex text-xl text-white p-2 justify-center text-center lg:gap-16">
      <a href="#" class="font-normal inline-block font-aboreto">New Covenant<span class="block font-sans font-normal bg-white mx-12 text-black">新約</span></a>
      <div
        class="absolute bg-black/50 lg:bg-transparent lg:text-start font-oswald font-medium p-2 lg:p-0 lg:static top-18 left-0 lg:top-auto lg:right-auto flex flex-col lg:flex-row lg:flex-1 lg:justify-end lg:place-items-center gap-4 lg:gap-16"
      >
        <a href="#app-section" class="flex lg:inline justify-between items-center gap-32 lg:gap-0 border-b lg:border-0 border-(--white-sub) text-red-500"
          >app<span class="lg:block text-xs font-sans font-normal under">アプリ</span></a
        >
        <a href="#about" class="flex lg:inline justify-between items-center gap-32"
          >about <span class="lg:block text-xs font-sans font-normal">アバウト</span></a
        >
        <a href="#operator" class="flex lg:inline justify-between items-center gap-32"
          >operator<span class="lg:block text-xs font-sans font-normal">オペレーター</span></a
        >
        <a href="#voice" class="flex lg:inline justify-between items-center gap-32">voice<span class="lg:block text-xs font-sans font-normal">ボイス</span></a>
        <a href="#gallery" class="flex lg:inline justify-between items-center gap-32"
          >gallery<span class="lg:block text-xs font-sans font-normal">ギャラリー</span></a
        >
      </div>
      <div class="flex flex-1 lg:flex-none place-items-center justify-end gap-8">
        <button><Share2 /></button>
        <button><AudioLines /></button>
        <button><User /></button>
      </div>
      <button class="lg:hidden text-4xl p-2"><Menu /></button>
    </div>
  </header>
</template>

<style scoped>
.font-aboreto {
  font-family: "Aboreto", cursive;
}

.font-oswald {
  font-family: "Oswald", sans-serif;
}
</style>
