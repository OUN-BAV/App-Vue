<template>
    <div class="card">
        <h3>{{card_data.first_Name}} {{card_data.last_Name}}</h3>
        <hr>
        <p>{{card_data.comment}}</p>
    </div>
</template>

<script>
export default {
  props:{
      card_data:Object,
  }

    
}
</script>

<style>
    .card {
        padding:10px;
        margin-top: 10%;
        margin-left: 15%;
        width:70%;
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
    }
</style>