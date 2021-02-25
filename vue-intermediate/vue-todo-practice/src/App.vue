<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput v-on:passNewItem="addList"></TodoInput>
    <TodoList></TodoList>
    <TodoFooter></TodoFooter>
  </div>
  
</template>

<script>
import TodoHeader from './components/TodoHeader.vue'
import TodoInput from './components/TodoInput.vue'
import TodoList from './components/TodoList.vue'
import TodoFooter from './components/TodoFooter.vue'

export default {

  data: function(){
    return {
      listItems: []
    }
  },

  methods: {
    addList: function(data){
      this.listItems.push(data);
    }
  },

  components: {
    'TodoHeader': TodoHeader,
    'TodoInput': TodoInput,
    'TodoList': TodoList,
    'TodoFooter': TodoFooter,
  }
}
</script>

<style>

</style>