<script setup>
import { ref } from 'vue'

const num = ref(true)

const list = ref('rice', 'beans', 'garri')

</script>

<template>
  <button @click="num = !num">Toogle list</button>
  <button @click="list.push (list.lenght + 1)">Push List</button>

  <button @click="list.pop ()">Pop List</button>
  <button @click="list.reverse()">Reverse List</button>

  <ul v-if="num && list.length">
    <li v-for="item of list">{{ item }}</li>

  </ul>
  <p v-else-if="list.length">The List Isn't Empty, just hidden</p>
  <p v-else>List is Empty</p>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
