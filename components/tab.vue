<template>
  <v-table density="compact">
    <thead>
      <tr>
        <th class="text-left">ID</th>
        <th class="text-left">TITLE</th>
        <th class="text-left">BODY</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="post in posts" :key="post.id" class="blue">
        <td>{{post.id}}</td>
        <td>{{post.title}}</td>
        <td>{{post.body}}</td>
      </tr>
  
    </tbody>
  </v-table>
</template>
<script setup>
const url = "https://jsonplaceholder.typicode.com/posts/";

// fetch
let posts = ref([]);
const { data } = await useFetch(url);
posts = data;
</script>
