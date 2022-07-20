<template>
  <input :type="InputType" :placeholder="InputPlaceHoler" v-model="mydata" @input="onchange"/>
</template>

<script>
export default {
    props:{
        InputType:String,
        InputPlaceHoler:String,
        value:String
    },
   data(){
    return{
        mydata:'',
    }
   },
   methods:{
    onchange(){
        this.$emit("getdata",this.mydata)
    }
   }
}
</script>

<style>
    input {
        margin-top: 10px;
    }
</style>