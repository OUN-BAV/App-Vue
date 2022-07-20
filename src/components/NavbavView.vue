<template>
    <ul>
        <List/>
    </ul>
</template>

<script>
import List from "./ListView.vue"
export default {
    components:{
        List
    }
}
</script>

<style>
  ul{
    display:flex;
    padding:15px;
    justify-content:space-around;
    background: rgb(253, 71, 71);
  }
</style>