<template>
  <div class="container">
    <!-- #3 must use the component-->
    <SevenWondersOfTheWorldHeader TitleName="SEVEN WONDERS OF THE WORLD"  />
 


    <SevenWondersOfTheWorldBox :SevenWondersOfTheWorld="SevenWondersOfTheWorld"  />
    <div class="About">
    <h1> <button><a href="https://ravikishorepathipati.herokuapp.com/"> Wanna know me ? </a></button> </h1>

    </div>


  </div>
 
</template>

<script>
import SevenWondersOfTheWorldHeader from './components/SevenWondersOfTheWorldHeader.vue'
import SevenWondersOfTheWorldBox from './components/SevenWondersOfTheWorldBox.vue'

export default {
  name: 'App',
  components: {
    SevenWondersOfTheWorldHeader,
    SevenWondersOfTheWorldBox
    
  },
  data(){
    return {
      SevenWondersOfTheWorld: []
    }
  },
  methods: {
    // promises

      async fetchSevenWondersOfTheWorld(){
        const res= await fetch('https://ravikishorepathipati.herokuapp.com/api')
        // const res= await fetch(' http://localhost:8000/api')
         const data= await res.json()
          console.log(data)
         return data.SevenWondersOfTheWorld
      }

  },

  async created(){
    this.SevenWondersOfTheWorld = await this.fetchSevenWondersOfTheWorld()
  }
}
</script>

<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0px;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 40px;
  border-radius: 5px;
  width:100%;
  background-color: white;
  background-image: url("https://thumbs.dreamstime.com/b/movie-reel-black-background-movie-reel-black-background-shadow-122061505.jpg");

}

div{
  margin-bottom: 0.5em;
  padding:10px;
}
.About{
  width:100%;
}
a{
    text-decoration: none;
    color: rgb(2, 7, 16);

}
button{
    font-size:30px;
    font-family:'Times New Roman', Times, serif;
    background-color: rgb(90, 50, 15);
    width:100%;
    border:3px solid rgb(212, 207, 165);


}



</style>

