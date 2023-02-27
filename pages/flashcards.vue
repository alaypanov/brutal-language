<template>
  <div class="w-full flex flex-col items-center justify-center h-full">
    <div class="relative w-80 h-120 flex-grow">
      <Deck v-for="card in cards" :key="card" @swipe="onSwipe">
        <Card :card="card" />
      </Deck>
    </div>
    <div>
      <button class="">Menu</button>
      <button>Next Deck</button>
    </div>
  </div>
</template>

<script>
import words from '../data/words';
const length = words.length;
const random = () => Math.floor(Math.random() * (length + 1));

export default {
  name: "App",
  data() {
    return { cards: [] };
  },
  mounted() {
    this.cards.push(words[random()]);
    this.cards.push(words[random()]);
  },
  methods: {
    onSwipe(direction) {
      this.cards.pop();
      this.cards.unshift(words[random()])
    },
  },
};
</script>