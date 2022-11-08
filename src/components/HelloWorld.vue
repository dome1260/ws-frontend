<template>
  <div>
    <button @click="update()"> Emit </button>
  </div>
</template>

<script>
export default {
  name: 'MyComponent',
  methods: {
    update () {


      this.$emit('my-event')


    }
  }
}
</script>
