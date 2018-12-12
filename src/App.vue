<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
<h1>{{this.xxx}}</h1>

  </div>
</template>

<script>
var xxx
export default {
  name: 'App',
 data() {
    return {
      xxx: 0
    }
  },
created() {
    this.property = 'Example property update.'
    console.log('propertyComputed will update, as this.property is now reactive.')
axios.get('https://api.coindesk.com/v1/bpi/currentprice.json', {
  method: 'get',
  headers: {
            'Content-Type': 'application/json',
        },
 mode:'no-cors',
  body:null
})
  .then(function(response) {
   this.xxx= (response.data.bpi);

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
