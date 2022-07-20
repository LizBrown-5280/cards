<template>
  <table v-if="amount">
    <tr>
      <td v-for="num in amount" :key="num" @click="updateSelectedCard(num)">{{ selectedCard(num) }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  name: 'Cards',
  props: {
    amount: Number
  },
  data() {
    return {
      cardSelected: 0,
    }
  },
  methods: {
    updateSelectedCard(num) {
      this.cardSelected = num;
    },
    selectedCard(num) {
      return num === this.cardSelected ? 'up' : 'down';
    }
  }
}
</script>

<style>
  td {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    border: 2px solid grey;
    text-align: center;
    cursor: pointer;
  }
  td:hover {
    background-color: rgba(255, 255, 255, 0.3);
  }
</style>
