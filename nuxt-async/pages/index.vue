<template>
  <section class="container">
    <div>
      <ul>
        <li v-for="user in users" :key="user.id">
          {{ user.id}}, {{ user.name }}, {{ user.company.name }}
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
const axios = require('axios')
let url = 'https://jsonplaceholder.typicode.com/usersxxx'
export default {
  asyncData({ params, error }) {
    return axios.get(url)
    .then((res) => {
      return { users: res.data }
    })
    .catch((e => {
      error({ users: e.response.status, message: 'Error!' })
    }))
  }
}
</script>

<style>
  ul {
    list-style: none;
  }
</style>