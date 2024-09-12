<script setup>
  import { ref } from 'vue'
  const list = ref([
    {
      id: 0, 
      img: '../src/assets/Image.png',
      alt: 'Title image One'
    }, {
      id: 1, 
      img: '../src/assets/Image-1.png', 
      alt: 'Title image Two'
    }, {
      id: 2, 
      img: '../src/assets/Image-2.png', 
      alt: 'Title image Three'
    }
  ])
</script>


<template>
  <section class="section_one">
    <h2>Section heading</h2>
    <ul>
      <li v-for="item in list" :key="item.id">
        <img :src="item.img" :alt="item.alt">
        <h3>Subheading</h3>
        <p>Body text for whatever you’d like to add more to the subheading.</p>
      </li>
    </ul>
  </section>
</template>


<style lang="scss">
  .section_one {
    margin-top: 150px;
    ul {
      display: flex;
      margin-top: 48px;
      gap: 32px;
      list-style: none;
      li {
        width: 405px;
        cursor: default;
        &::after {
          content: none;
        }
        img {
          width: 405px;
          height: auto;
        }
        h3 {
          font-size: 24px;
          color: var(--c-black);
          line-height: 1.5;
          font-weight: 600;
        }
        p {
          margin-top: 4px;
          font-size: 24px;
          color: var(--c-grey);
          line-height: 1.5;
          font-weight: 400;
        }
      }
    }
  }
</style>