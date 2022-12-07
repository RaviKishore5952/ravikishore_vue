<template>
    <!--div v-if="book.published == false"-->


<div class="SevenWondersOfTheWorld">
    <ul><h1 style="color:cadetblue">{{SevenWondersOfTheWorld.name}}</h1></ul>
    <ul><h4>History : {{SevenWondersOfTheWorld.History}}</h4></ul>
    <ul><h4>city : {{SevenWondersOfTheWorld.city}}</h4></ul>
    <ul><h4>country : {{SevenWondersOfTheWorld.country}}</h4></ul>
    <ul><h4>Image : {{SevenWondersOfTheWorld.Image}}</h4></ul>
    <ul><h4>Time :  {{SevenWondersOfTheWorld.Time}}</h4></ul>
    </div>
</template>

<script>

export default{
    name: 'SevenWondersOfTheWorld',
    props:{
        SevenWondersOfTheWorld: Array
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

.SevenWondersOfTheWorld{
    background-color: #01040a;
    
    color:rgb(60, 86, 135);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width:100%;
    height: 375px;;
}
.SevenWondersOfTheWorld:hover {
    border: 5px solid rgb(149, 107, 98);
 color: rgb(81, 17, 23);
 box-shadow: 8px 8px rgb(46, 46, 45);
}

</style>