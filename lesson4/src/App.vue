<template>
  <div id="app">
    <TodoList :shop="shop" @delete-item="deleteItem"/>
    <New :vata="vata" @del="dele" />
    <hehader :kaka="kaka" @dk="delkk"/>
    <mat :waiting="waiting"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import New from './components/new'
import hehader from './components/header.vue'
import mat from './components/mat.vue'

export default {
  name: 'App',
  data(){
    return{
      shop: ['aaaa', 'bbbb', 'cccc'],
      vata: ['v', 'a', 't', 'a'],
      kaka: ['kkk', 'aaaa', 'bbbbbbbbbbb'],
      waiting: 'eb vahsu nalevo nahuy'
    }
  },
  components: {
    TodoList,
    New,
    hehader,
    mat
  },
  methods: {
    deleteItem(index) {
      this.shop.splice(index, 1);
    },
    dele(p){
      this.vata.splice(p, 1);
    },
    delkk(o){
      this.kaka.splice(o, 1);
    }
  }
} 
</script> 

<style lang="css">
#app {
  max-width: 500px;
  margin: 0 auto;
}
</style>
