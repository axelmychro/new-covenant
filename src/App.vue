<script setup>
import { User, AudioLines, Share2 } from "lucide-vue-next";
</script>

<template>
  <header>
    <div class="bg-black font-medium uppercase fixed top-0 left-0 w-full flex text-xl text-white lg:p-4 justify-center text-center">
      <a href="#" class="lg:text-2xl font-normal inline-block  font-aboreto">New Covenant<span class="block bg-white mx-16 text-black">新約</span></a>
      <div
        class="absolute bg-black lg:bg-transparent p-2 lg:p-0 lg:static top-16 right-12 lg:top-auto lg:right-auto z-50 flex flex-col lg:flex-row lg:flex-1 lg:justify-end place-items-start lg:place-items-end gap-4 lg:gap-8"
      >
        <a href="#app" class="text-red-500">app<span class="block text-xs ">アプリ</span></a>
        <a href="#about" class="">/about<span class="block text-xs">アバウト</span></a>
        <a href="#operator" class="">/operator<span class="block text-xs">オペレーター</span></a>
        <a href="#voice" class="">/voice<span class="block text-xs">ボイス</span></a>
        <a href="#gallery" class="">/gallery<span class="block text-xs">ギャラリー</span></a>
      </div>
      <div class="flex flex-1 lg:flex-none place-items-center justify-end gap-8 lg:pl-8 pr-2">
        <a href="#" role="button"><Share2 /></a>
        <a href="#" role="button"><AudioLines /></a>
        <a href="#" role="button"><User /></a>
      </div>
      <button class="lg:hidden text-4xl border-white border-l-2 border-b-2 p-2">≡</button>
    </div>

    <div><h1>Exusiai</h1></div>
  </header>
  <main class="bg-red-500">
    <section class="">
      <h2>Apple Pie</h2>
      <img src="./assets/images/26_g12_laterano_office.png" alt="wahoo" class="w-full" />
    </section>
    <div class="">1</div>
  </main>
  <footer class="">
    <div class="w-full h-4 bg-yellow-500 z-10 text-white">footer</div>
  </footer>
</template>
