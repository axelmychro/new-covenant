<template>
  <div id="container"><div id="diamond"></div></div>
</template>

<style scoped>
  div {
    width: 8rem;
    height: 8rem;
    aspect-ratio: 1/1;
    background-color: var(--logo-in);
  }
  #container {
    background-color: var(--logo-in);
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 2%;
  }
  #diamond {
    border: 8px solid var(--logo-out);
    transform: rotate(45deg);
    background-color: var(--logo-in);
    width: 50%;
    height: 50%;
  }
</style>
