<template>
  <div>jokes :

    <Joke v-for="joke in jokes" :key="joke.id" :joke="joke.joke" />
  </div>

</template>
<script>
  import axios from "axios";
  import Joke from "~/components/Joke";

  export default{
    data(){
      return{
        jokes : []
      }
    },
    components:{
      Joke
    },
    async created(){
      const config = {
        headers: {
          Accept: "application/json"
        }
      };

      try{
        const res = await axios.get('https://icanhazdadjoke.com/search', config);
        const data = res.data.results;
        this.jokes = data;
      }catch(err){
        console.log(err);
      }
    },
    head(){
      return {
        title: 'Dad Jokes',
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'Best place for corny dad jokes'
          }
        ]
      }
    }
  };
</script>

<style></style>
