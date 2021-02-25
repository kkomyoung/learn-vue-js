<template>
  <div>
    <input v-model="newItem" v-on:keyup.enter="addItem" type="text" placeholder="할 일을 입력해주세요.">
    <button v-on:click="addItem">추가</button>
  </div>
</template>

<script>
export default {
  data: function(){
    return {
      newItem: '',
    }
  },

  methods: {
    addItem: function(){
      this.$emit('passNewItem', this.newItem);
      localStorage.setItem(this.newItem, this.newItem);
      this.clearItem();
    },
    clearItem: function(){
      this.newItem = '';
    }
  }
}
</script>

<style>

</style>