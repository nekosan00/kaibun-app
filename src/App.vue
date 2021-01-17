<template>
  <div id="app">
    <h1>回文作成</h1>
    <p>{{ f }}</p>
    <input v-model="k">
    <button v-on:click="reverseMessage">生成</button>
    <button v-on:click="reverseMessageT">だぶらせずに生成</button>
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
            background-color: black;
            color: white;
            text-align: center;
            margin: 5%;
}
</style>
