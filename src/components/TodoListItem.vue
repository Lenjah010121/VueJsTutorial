<template>
<div class="borderBold">
 <li :class="{'finishedTask':item.finished}">
   <input type="checkbox" :checked="item.finished"/>
   <button @click="toggleItem">toggle</button>
   {{item.name}}
 </li>
</div>
</template>

<script>
export default {
  name: "TodoListItem",
  props: ["item"],
  methods:{
    toggleItem(){
       this.$emit('toggle', this.item)
    }
  }
};
</script>

<style>
</style>