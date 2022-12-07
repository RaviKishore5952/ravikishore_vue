<template>  
    <div class="SevenWondersOfTheWorldBox">
       <div v-for="SevenWondersOfTheWorld in SevenWondersOfTheWorld" :key="SevenWondersOfTheWorld.ID" >     
               <SevenWondersOfTheWorld :SevenWondersOfTheWorld="SevenWondersOfTheWorld"/>
       </div> 
    </div>
</template>
<script>
import SevenWondersOfTheWorld from "./SevenWondersOfTheWorld.vue"
export default{
   name: 'SevenWondersOfTheWorldBox',
   components: {
    SevenWondersOfTheWorld
   },
   props: {
    SevenWondersOfTheWorld: Array
   }
}
</script>
<style>
.SevenWondersOfTheWorldBox{

 padding: 40px;
    color: gray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    border:3px solid rgb(29, 70, 127);
    background-image: url("https://static01.nyt.com/images/2017/12/01/travel/360-7wondersmap3/360-7wondersmap3-jumbo.png");
    background-repeat: no-repeat;
    background-attachment: fixed;  
    background-size: cover;
   
}
</style>