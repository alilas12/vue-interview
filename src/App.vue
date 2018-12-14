<template>
  <div id="app">
    <Menu></Menu>
    
    <div class="item-creator">
      <input type="text">
      <button>
        Add
      </button>
    </div>

    <Item v-for="item in items" :key="item">{{item}}</Item>

    <Footer></Footer>
  </div>
</template>

<script>
import Menu from './components/Menu';
import Item from './components/Item';
import Footer from './components/Footer';

export default {
  name: 'app',
  components: {
    Menu,
    Item,
    Footer
  },

  data() {
    return {
      items: [
        'Wash car', 
        'Do groceries', 
        'Finish this assignment'
      ]
    }
  }
}
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
}

* {
  box-sizing: border-box;
}
#app {

  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#app .item-creator {
  height: 4rem;
  line-height: 4rem;
}
</style>
