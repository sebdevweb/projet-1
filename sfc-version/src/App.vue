<script setup>
  import { ref } from 'vue'
  import Header from './components/Header.vue'
</script>

<template>
  <Header />
  <main>
    <article>
      <h1>Landing page title</h1>
      <p>Subheading that sets up context, shares more info about the website, or generally gets people psyched to keep scrolling.</p>
      <button class="btn_big">Button</button>
      <img src="./assets/Hero Image.png" alt="Hero Landingpage">
    </article>
  </main>
</template>

<style lang="scss">
:root {
 --font-400: 400;
 --font-500: 500;
 --font-700: 700;

 --c-black: #000;
 --c-black75: rgba(0, 0, 0, .75);
 --c-black50: rgba(0, 0, 0, .5);
 --c-grey: #828282;
 --c-second-grey: #e6e6e6;
 --c-third-grey: #d9d9d9;
 --c-light-grey: #f7f7f7;
 --c-white: #fff;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Inter", sans-serif;
}

#app {
  max-width: 1440px;
  margin: 0 auto;
  background: var(--c-white);
  box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
}

/* MAIN: article */
article {
  padding: 0 80px;
  h1 {
    font-size: 64px;
    color: var(--c-black);
    line-height: auto;
    letter-spacing: -2px;
  }
  p {
    margin-top: 24px;
    font-size: 24px;
    color: var(--c-black75);
    font-weight: 400;
    max-width: 844px;
  }
  button {
    margin: 40px 0 80px; 
    &.btn_big {
      font-size: 24px;
      padding: 20px 32px;
    }
  }
  img {
    max-width: 1280px;
    height: auto;
  }
}

/* Global style for button */ 
button {
  background: var(--c-black);
  color: var(--c-white);
  border-radius: 8px;
  border: none;
  cursor: pointer;
  transition: .2s ease-out;
  &:hover {
    background: var(--c-third-grey);
    color: var(--c-black75);
    transition: .3s ease-in;
  }
  &.btn_std {
    font-size: 16px;
    padding: 14px 24px;
  }
}
</style>
