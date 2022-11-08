<template>
  <div id="app">
    <h1> Test socket </h1>
    <div v-for="(msg, i) in messages" :key="i">
      {{ msg }}
    </div>
  </div>
</template>

<script>
import io from 'socket.io-client'

export default {
  name: 'App',
  data () {
    return {
      messages: []
    }
  },
  created () {
    const socket = io('http://localhost:3000')
    socket.on('test', (data) => {
      this.messages.push(data)
    })
  },
}
</script>

<style scoped>

</style>
