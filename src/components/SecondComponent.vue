<template>
    <div style="border: 1px solid black;">
        <h1>Second Component</h1>
        <button v-on:click="emitMyEvent">Emit Event</button>
    </div>
</template>

<script>
    export default {
        data: function () {
    return {
      contar: Number = 1
    }
  },
        methods: {
          emitMyEvent() {
              this.emitter.emit('my-event', {'eventContent': 'String changed: ' + this.contar ++})
          }
        }
    }
</script>

<style scoped>

</style>
