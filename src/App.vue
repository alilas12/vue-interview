<template>
  <b-container fluid class="text-center vh-100">
    <b-row class="h-10">
      <Menu></Menu>
    </b-row>

    <b-row class="d-flex justify-content-center h-10">
      <ItemCreator :input="input" :items="items"></ItemCreator>
    </b-row>

    <b-row v-b-scrollspy:nav-scroller>
      <Item :class="{'color': index % 2 }" v-for="(item, index) in items" :key="index">
        <b-col v-b-modal.itemModal cols="8" class="float-left">
          <span class="text-break">{{item}}</span>
        </b-col>
        <b-col cols="4" class="float-left w-100">
          <b-button @click="deleteItem(index)" variant="danger" class="float-right">Delete</b-button>
        </b-col>
      </Item>
    </b-row>

    <b-row>
      <Footer></Footer>
    </b-row>

    <b-modal id="itemModal">
      <p></p>
    </b-modal>
    
  </b-container>
</template>

<script>
import Menu from './components/Menu';
import Item from './components/Item';
import Footer from './components/Footer';
import ItemCreator from './components/ItemCreator';

export default {
  name: 'app',
  components: {
    Menu,
    Item,
    Footer,
    ItemCreator
  },

  data() {
    return {
      input: '',
      items: [],
    }
  },

  mounted() {
    if(localStorage.items){
      this.items = JSON.parse(localStorage.items);
    }
  },

  watch:{
    items(oldItems) {
      localStorage.items = JSON.stringify(oldItems);
    }
  },

  methods: {
    deleteItem(index) {
      this.items.splice(index, 1);
    },
    handleScroll () {
      this.scrolled = window.scrollY > 0;
    },
  },
}
</script>

<style lang="scss">
  .color{
    background-color: #e0e0e0;
  }
  .h-10{
    height: 10%;
  }
</style>
