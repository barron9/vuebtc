<template>
  <div id="app">
{{this.xxx.data}}

  </div>
</template>

<script>
var xxx
export default {
  name: 'App',
 data() {
    return {
property:null,
      xxx: '***'
    }
  },
created() {
var self= this
    self.property = 'Example property update.'
    console.log('starting pull')
axios.get('http://127.0.0.1:3000' )
  .then(function(response) {
   self.xxx= (response);

  })

  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
