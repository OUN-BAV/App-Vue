<template>
  <form @submit.prevent="onAdd" class ="form-group">
        <Input type="text" placeholder="firstname" class="form-control" :value="getdata" v-model="firstname"/>
        <Input type="text" placeholder="lastname" class="form-control" :value="getdata" v-model="lastname"/>
        <Input type="text" placeholder="comment" class="form-control" :value="getdata" v-model="comment"/>
        <Button buttonName="Add" buttonBackground="grey" class="form-control" />
  </form>
</template>

<script>
import Button from "./ButtonView.vue"
import 'bootstrap'
import 'bootstrap/dist/css/bootstrap.min.css'
import Input from "./InputView.vue"
export default {
    emits:["newList"],
    components:{
        Input,
        Button,
    },
    data(){
        return {
            firstname:"",
            lastname:"",
            comment:""
        }

    },
    methods:{
        onAdd(e){
            e.preventDefault();
            this.$emit("newList",this.firstname,this.lastname,this.comment)
        }
    }
   

}
</script>

<style>
    form{
        padding:10px;
        margin-top: 10%;
        margin-left: 15%;
        width:70%;
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

    }
</style>