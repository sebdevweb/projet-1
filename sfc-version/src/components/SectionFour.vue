<script setup>
  function notify() {
    alert('Votre mail a été envoyé avec succès !')
  }
</script>


<template>
  <section class="section_four">
    <h2>Add your email for receive notifications</h2>
    <form>
      <fieldset>
        <label for="email">Your email</label>
        <input type="email" placeholder="Add your email">
        <button @click.prevent="notify">Send</button>
      </fieldset>
    </form>
  </section>
</template>


<style lang="scss">
  .section_four {
    background: var(--c-light-grey);
    padding: 48px;
    margin-top: 150px;
    h2 {
      margin-bottom: 48px;
    }
    form {
      width: 50%;
      margin-bottom: 48px;
      fieldset {
        border: none;
        display: flex;
        gap: 24px;
        align-items: center;
        label {
          font-size: 24px;
        }
        input {
          height: 48px;
          border-radius: 4px;
          border: 1px solid var(--c-black75);
          flex: 1 0 auto;
          padding: 0 12px;
          font-size: 24px;
          &::placeholder {
            color: var(--c-grey);
            font-size: 20px;
          }
          &:focus-visible {
            border: 2px solid var(--c-second-grey);
          }
        }
        button {
          padding: 12px 32px;
          font-size: 20px;
          max-width: 200px;
          &:hover {
            background: var(--c-black50);
            color: var(--c-white);
          }
        }
      }
    }
  }
</style>