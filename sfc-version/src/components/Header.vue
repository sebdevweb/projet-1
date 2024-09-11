<script setup>
  import { ref } from 'vue'

  const navList = ref([
    {id: 0, text: 'Page One'},
    {id: 1, text: 'Page Two'},
    {id: 2, text: 'Page Three'},
    {id: 2, text: 'Page Four'}
  ])

</script>

<template>

  <header>
    <div class="logo">Site name</div>
    <nav>
      <ul>
        <li v-for="itemNav in navList" :key="itemNav.id">{{ itemNav.text }}</li>
      </ul>
      <button class="btn_std" type="button>">Button</button>
    </nav>
  </header>

</template>

<style lang="scss">
  header {
  height: 164px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 80px;
  
  .logo {
    font-size: 20px;
    color: var(--c-black);
    font-weight: 500;
  }
  nav {
    display: flex;
    align-items: center;
    ul {
      list-style: none;
      display: flex;
      gap: 48px;
      li {
        font-size: 20px;
        font-weight: 500;
        color: var(--c-black);
        cursor: pointer;
        position: relative;
        transition: .2s ease-out;
        &:hover {
          color: var(--c-black50);
          transition: .3s ease-in;
          &::after {
            background: var(--c-black50);
            content: '';
            position: absolute;
            width: 100%;
            height: 2px;
            left: 0;
            bottom: -10px;
            transition: .3s ease-in;
          }
        }
        &::after {
          width: 0;
          position: absolute;
          content: '';
          transition: .2s ease-out;
        }
      }
    }
    button {
      margin-left: 48px;
    }
  }
}
</style>