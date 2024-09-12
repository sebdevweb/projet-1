<script setup>
  import { ref } from 'vue'

  const listTwo = ref([
    {text: 'Body text for whatever you’d like to expand on the main point.'},
    {text: 'Body text for whatever you’d like to say. Add main takeaway points, quotes, anecdotes.'},
    {text: 'Body text for whatever you’d like to add more to the main point. It provides details, explanations, and context.'},
  ])
</script>


<template>
  <section class="section_two">
    <div class="section_two--group">
      <div class="left">
        <h2>Section heading</h2>
        <div v-for="itemTwo in listTwo" :key="index">
          <h3>Subheading</h3>
          <p>{{ itemTwo.text }}</p>
        </div>
        <div class="actions">
          <button class="btn_std" type="button">Button</button>
          <button class="btn_std--secondary" type="button">Secondary button</button>
        </div>
      </div>
      <div class="right">
        <img src="../assets/Image-3.png" alt="Image section two">
      </div>
    </div>
  </section>
</template>


<style lang="scss">
  .section_two {
    margin-top: 150px;
    &--group {
      display: flex;
      margin-top: 48px;
      gap: 140px;
      .left {
        max-width: 516px;
        h2 {
          margin-bottom: 48px;
        }
        div {
          h3 {
            font-size: 24px;
          }
          p {
            color: var(--c-grey);
            margin-top: 8px;
          }
          &:not(:last-child) {
            margin-bottom: 48px;
          }
        } 
        .actions {
          display: flex;
          gap: 16px;
          .btn_std, .btn_std--secondary {
            font-size: 24px;
          } 
          .btn_std--secondary {
            background: var(--c-third-grey);
            color: var(--c-black);
            padding: 14px 24px;
          }
          .btn_std--secondary:hover {
            background: var(--c-second-grey);
          }
        }
      }
      .right {
        width: 50%;
        img {
          width: 100%;
        }
      }
    }
  }
</style>