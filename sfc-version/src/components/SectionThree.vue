<script setup>
  import { ref } from 'vue'

  const listThree = ref([
    {
      text: '“A terrific piece of praise”', 
      name: 'John', 
      desc: 'lorem ipsum', 
      img: 'src/assets/Avatar.png'
    }, {
      text: '“A fantastic bit of feedback”', 
      name: 'Jane', 
      desc: 'sit dolor amet', 
      img: 'src/assets/Avatar-1.png'
    }, {
      text: '“A genuinely glowing review”', 
      name: 'Mary', 
      desc: 'consectetur adipisicing elit', 
      img: 'src/assets/Avatar-2.png'
    }
  ])
</script>


<template>
  <section class="section_three">
    <h2>Section heading</h2>
    <div class="section_three--group">
      <div v-for="itemThree in listThree" :key="index" class="item">
        <h3>{{ itemThree.text}}</h3>
        <div class="item--group">
          <img :src="itemThree.img" :alt="itemThree.name">
          <h4>{{ itemThree.name }}</h4>
          <p>{{ itemThree.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss">
  .section_three {
    margin-top: 150px;
    h2 {
      margin-bottom: 48px;
    }
    &--group {
      display: flex;
      gap: 32px;
      margin-top: 48px;
      .item {
        border: 1px solid var(--c-third-grey);
        border-radius: 12px;
        padding: 32px;
        max-width: 405px;
        width: 100%;
        h3 {
          margin-bottom: 48px;
        }
        &--group {
          display: grid;
          grid-template-columns: repeat(6, 1fr);
          max-width: 340px;
          img {
            grid-column: 1 / 3;
            grid-row: 2;
            width: 45px;
            height: auto;
          }
          h4 {
            grid-column: 2;
            grid-row: 2;
            font-size: 16px;
          }
          p {
            grid-column: 2 / 7;
            grid-row: 2;
            font-size: 16px;
            color: var(--c-grey);
          }
        }
      }
    }
  }
</style>