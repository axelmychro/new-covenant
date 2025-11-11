<script setup>
import Section from "./main/Section.vue";

import bgApp from "../assets/images/26_g12_laterano_office.png";
import bgAbout from "../assets/images/cery.png";
import bgOperator from "../assets/images/seren.png";
import bgVoice from "../assets/images/style.jpg";
import bgGallery from "../assets/images/lemus.jpg";
import { ref, onMounted } from "vue";

const mainRef = ref(null);

const handleKeyDown = (e) => {
  if (!mainRef.value) return;

  if (e.key === "ArrowUp" || e.key === "ArrowLeft") {
    e.preventDefault();
    mainRef.value.scrollBy({ left: -window.innerWidth, behavior: "smooth" });
  } else if (e.key === "ArrowDown" || e.key === "ArrowRight") {
    e.preventDefault();
    mainRef.value.scrollBy({ left: window.innerWidth, behavior: "smooth" });
  }
};

const handleWheel = (e) => {
  if (!mainRef.value) return;
  e.preventDefault();
  mainRef.value.scrollBy({ left: e.deltaY > 0 ? window.innerWidth : -window.innerWidth, behavior: "smooth" });
};

onMounted(() => {
  window.addEventListener("keydown", handleKeyDown);
  if (mainRef.value) {
    mainRef.value.addEventListener("wheel", handleWheel, { passive: false });
  }
});
</script>

<template>
  <main ref="mainRef" class="flex h-screen overflow-x-scroll snap-x snap-mandatory scrollbar-hide">
    <Section id="app-section" :bg="bgApp" class="min-w-full">
      <h1>App</h1>
    </Section>

    <Section id="about" :bg="bgAbout" class="min-w-full">
      <h2>About</h2>
    </Section>

    <Section id="operator" :bg="bgOperator" class="min-w-full">
      <h2>Operator</h2>
    </Section>

    <Section id="voice" :bg="bgVoice" class="min-w-full">
      <h2>Voice</h2>
    </Section>

    <Section id="gallery" :bg="bgGallery" class="min-w-full">
      <h2>Gallery</h2>
    </Section>
  </main>
</template>
