<script setup>
import Section from "./main/Section.vue";
import bgImage from "@/assets/images/26_g12_laterano_office.png";
</script>

<template>
  <main class="h-screen overflow-y-scroll snap-y snap-mandatory">
    <Section id="app-section" :bg="bgImage">
      <h1>App</h1>
    </Section>

    <Section id="about" :bg="bgImage">
      <h2>About</h2>
    </Section>

    <Section id="operator" :bg="bgImage">
      <h2>Operator</h2>
    </Section>

    <Section id="voice" :bg="bgImage">
      <h2>Voice</h2>
    </Section>

    <Section id="gallery" :bg="bgImage">
      <h2>Gallery</h2>
    </Section>
  </main>
</template>
