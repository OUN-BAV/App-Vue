<template>
  <button :style="{background:buttonBackground}" >{{buttonName }}</button>
</template>

<script>
export default {
    props:{
        buttonBackground:String,
        buttonName:String
    }
}
</script>

<style>
  button{
    margin-top: 10px;
  }
</style>