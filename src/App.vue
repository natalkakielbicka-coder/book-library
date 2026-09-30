<script setup>
import { ref } from 'vue'
import BookItem from './components/BookItem.vue'

const books = ref([
  {
    id: 1,
    title: 'Solaris',
    author: 'Stanisław Lem',
    status: 'Przeczytane',
  },
  {
    id: 2,
    title: 'Lalka',
    author: 'Bolesław Prus',
    status: 'Czytam',
  },
  {
    id: 3,
    title: 'Pan Tadeusz',
    author: 'Adam Mickiewicz',
    status: 'Chcę przeczytać',
  },
])
</script>

<template>
  <main class="app">
    <h1>Biblioteka książek</h1>

    <ul class="book-list">
      <BookItem v-for="book in books" :key="book.id" :book="book" />
    </ul>
  </main>
</template>

<style scoped>
.app {
  max-width: 720px;
  margin: 0 auto;
  padding: 40px 20px;
}

.book-list {
  margin: 0;
  padding: 0;
  list-style: none;
}
</style>
