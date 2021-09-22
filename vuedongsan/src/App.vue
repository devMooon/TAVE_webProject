<template>
  <div id="app">
    <div class="menu">
      <a v-for="(a, i) in menus" :key="i">{{a}}</a>
    </div>

    <div v-for="(a, i) in 3" :key="i">
      <h4>{{products[i]}}</h4>
      <p>{{price[i]}} 만원</p>
      <button @click="increase(i)">허위매물신고</button> <span>신고수 : {{신고수[i]}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return{
      신고수 : [0, 0, 0],
      menus : ['Home', 'Shop', 'About'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      price : [70, 60, 50],
    }
  },
  methods : {
    increase(index) {
      this.신고수[index] += 1;
    },
  },
  components: {
  }
}
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
.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
