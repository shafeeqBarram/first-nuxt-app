<template>
  <div>
    <h1>Welcome to our app</h1>
    <ul>
      <li v-for="fact in facts">{{fact.text}}</li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  head(){
    
    return{
      title:"Welcome to our first nuxt app"
    }
  },
  async asyncData(){
    const response = await axios.get("https://nuxt-ssr.firebaseio.com/facts.json")
    const facts = response.data
    console.log(facts);
    return {facts}
  },
  components: {

  }
}
</script>

<style>

</style>
