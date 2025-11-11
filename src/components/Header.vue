<script setup>
import { Share2, AudioLines, User, Menu } from "lucide-vue-next";
import { ref, onMounted, onUnmounted } from "vue";

const currentSection = ref("app-section");

const handleScroll = () => {
  const sections = ["app-section", "about", "operator", "voice", "gallery"];
  const scrollContainer = document.querySelector("main");

  if (scrollContainer) {
    const containerRect = scrollContainer.getBoundingClientRect();

    for (const sectionId of sections) {
      const section = document.getElementById(sectionId);
      if (section) {
        const rect = section.getBoundingClientRect();
        if (rect.left <= containerRect.left + containerRect.width / 2 && rect.right >= containerRect.left + containerRect.width / 2) {
          currentSection.value = sectionId;
          break;
        }
      }
    }
  }
};

const navigateToSection = (sectionId) => {
  const element = document.getElementById(sectionId);
  if (element) {
    const scrollContainer = document.querySelector("main");
    if (scrollContainer) {
      const offset = element.offsetLeft;
      scrollContainer.scrollTo({ left: offset, behavior: "smooth" });
    }
  }
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll, true);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll, true);
});
</script>

<template>
  <header>
    <div class="bg-black/50 z-50 uppercase fixed top-0 left-0 w-full h-20 flex text-xl text-white p-2 justify-center text-center lg:gap-16">
      <a href="#" class="font-normal inline-block font-aboreto">New Covenant<span class="block font-sans font-normal bg-white mx-12 text-black">新約</span></a>
      <div
        class="absolute bg-black/50 lg:bg-transparent lg:text-start font-oswald font-medium p-2 lg:p-0 lg:static top-18 left-0 lg:top-auto lg:right-auto flex flex-col lg:flex-row lg:flex-1 lg:justify-end lg:place-items-center gap-4 lg:gap-16"
      >
        <a
          href="#"
          @click.prevent="navigateToSection('app-section')"
          class="flex lg:inline justify-between items-center gap-32 lg:gap-0 border-b lg:border-0 border-(--white-sub) transition-colors hover:text-red-500 cursor-pointer"
          :class="{ 'text-red-500': currentSection === 'app-section', 'text-white': currentSection !== 'app-section' }"
          >app<span class="lg:block text-xs font-sans font-normal under">アプリ</span></a
        >
        <a
          href="#"
          @click.prevent="navigateToSection('about')"
          class="flex lg:inline justify-between items-center gap-32 transition-colors hover:text-red-500 cursor-pointer"
          :class="{ 'text-red-500': currentSection === 'about', 'text-white': currentSection !== 'about' }"
          >about <span class="lg:block text-xs font-sans font-normal">アバウト</span></a
        >
        <a
          href="#"
          @click.prevent="navigateToSection('operator')"
          class="flex lg:inline justify-between items-center gap-32 transition-colors hover:text-red-500 cursor-pointer"
          :class="{ 'text-red-500': currentSection === 'operator', 'text-white': currentSection !== 'operator' }"
          >operator<span class="lg:block text-xs font-sans font-normal">オペレーター</span></a
        >
        <a
          href="#"
          @click.prevent="navigateToSection('voice')"
          class="flex lg:inline justify-between items-center gap-32 transition-colors hover:text-red-500 cursor-pointer"
          :class="{ 'text-red-500': currentSection === 'voice', 'text-white': currentSection !== 'voice' }"
          >voice<span class="lg:block text-xs font-sans font-normal">ボイス</span></a
        >
        <a
          href="#"
          @click.prevent="navigateToSection('gallery')"
          class="flex lg:inline justify-between items-center gap-32 transition-colors hover:text-red-500 cursor-pointer"
          :class="{ 'text-red-500': currentSection === 'gallery', 'text-white': currentSection !== 'gallery' }"
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
