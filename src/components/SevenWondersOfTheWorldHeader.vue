<template>
    <div>
        <h1> {{TitleName}} </h1>
    
    </div>
    </template>
    
    <script>
    
    export default{
        name: 'SevenWondersOfTheWorldHeader',
        props:{
            TitleName: String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
        color: rgb(180, 49, 10);
        font-family: 'Times New Roman', Times, serif;
    }
    
    </style>