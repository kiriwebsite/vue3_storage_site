<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

const comments = ref([])

onMounted(async () => {
  const res = await axios.get('http://localhost:3000/api/comments')
  comments.value = res.data
})
</script>

<template>
  <div>
    <h1>評論清單</h1>
    <ul>
      <li v-for="comment in comments" :key="comment._id">
        <b>{{ comment.name }}</b>：{{ comment.text }}
      </li>
    </ul>
  </div>
</template>
