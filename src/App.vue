<template>
  <Nav/>
  <Form @newList = "addList"/>
  <Card v-for ="(list,index) of lists" :key="index" :card_data="list" />
</template>

<script>
import Card from "./components/CardView.vue"
import Nav from "./components/NavbavView.vue"
import Form from "./components/FormView.vue"
export default {
  components: {
   Form,Nav,Card
  },
  data(){
    return{
      lists:[
        {first_Name:'Oun',last_Name:'Bav',comment:'Oun is handsome'},
        {first_Name:'Oun',last_Name:'Bav',comment:'Oun is handsome'},
        {first_Name:'Oun',last_Name:'Bav',comment:'Oun is handsome'},
        ],
        list:'',
    }
  },
  methods:{
    addList(firstname,lastname,comment){
      console.log(firstname,lastname,comment);
      this.lists.push({first_Name:firstname,last_Name:lastname,comment:comment});
    }
  }
  
}
</script>

<style>
#app {
  margin-top:10%;
  margin-left: 25%;
  padding:20px;
  width: 50%;
  border: 1px solid rgb(247, 63, 63);
  border-style: dashed;
  border-radius: 20px;
}
</style>
