<script setup>
import Nav from './components/Nav.vue'
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <Nav></Nav>
  </header>

  <main>
  </main>
</template>

<style scoped>
header {
  background-color: red;
  /* line-height: 1.5; */
}


@media (min-width: 1024px) {
  header {
    /* display: flex; */
    /* place-items: center; */
    /* padding-right: calc(var(--section-gap) / 2); */
  }

}
</style>
