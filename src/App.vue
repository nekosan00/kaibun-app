<template>
  <div id="app">
  <h1>回文生成</h1>

  </div>
</template>

<script>
  var app = new Vue({
    el: '#app',
    data: {
        m: '',
        f: '',
        t: '',
        s: '',
        p: '',


    },
    methods: {
        reverseMessage: function () {
            this.m = this.k.split('').reverse().join('');  
            this.f = this.k.concat(this.m);
        } ,
        reverseMessageT: function () {
            this.m = this.k;
            this.t = this.m.slice( 0, -1 ) ;
            this.s = this.t.split('').reverse().join(''); 
            this.f = this.m.concat(this.s);
                
        }
    }


})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
