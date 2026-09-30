<script setup>
defineProps({
  book: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <li class="book-item">
    <strong>{{ book.title }}</strong>
    <span>{{ book.author }}</span>
    <span>{{ book.status }}</span>
  </li>
</template>

<style scoped>
.book-item {
  display: flex;
  gap: 16px;
  padding: 14px 0;
  border-bottom: 1px solid #ddd;
}
</style>
