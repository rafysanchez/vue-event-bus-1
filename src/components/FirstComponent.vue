<script>
export default {
  data: function () {
    return {
      testEvent: 'String to change'
    }
  },
  created (){
    this.emitter.on('my-event', (evt) => {
      this.testEvent = evt.eventContent;
    })
  }
}
</script>

<template>
  <div style="border: 1px solid black;">
    <h1>First Component</h1>
    <p>{{testEvent}}</p>
  </div>
</template>

<style scoped>
div{
  border-radius: 16px;
  background-color: orange;
}
p{
  font-weight: 900;
}
a {
  color: #42b983;
}

</style>
