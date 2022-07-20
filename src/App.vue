<template>
  <header>
    <h1>Card Game</h1>
  </header>

  <main>
    Number of cards: <input v-model.number="amount" type="number" />
    <Cards :amount=amount />
  </main>
</template>

<script>
import Cards from '@/components/Cards.vue';

export default {
  name: 'Home',
  components: { Cards },
    data() {
    return {
      amount: 3
    }
  }
}
</script>

<style>
  input {
    width: 45px;
  }
</style>
