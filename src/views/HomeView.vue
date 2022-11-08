<template>
  <div class="home">
    <div v-for="(item, i) of items" :key="i">
      <!-- <input type="text" v-model="items[i]"> -->
      {{ i }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'HomeView',
  data () {
    return {
      items: [
        '',
        ''
      ]
    }
  }
}
</script>
