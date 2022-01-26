<!-- Please remove this file from your project -->
<template>
  <div class="grid grid-cols-3 gap-2 mt-5 p-5">
      <Card v-for="mountain in mountains" v-bind:id="mountain.slug" v-bind:key="mountain.slug" v-bind:slug="mountain.slug" v-bind:mountain="mountain"/>
  </div>
   
</template>



<script>

import Card from './cards/Card'

  export default {
    name: 'CardsList',
    components: {
      Card
    },
    data() {
      return { 
        mountains: [],
      }
    },
    async created() {
      try {
         const mountains = await fetch(
        'https://api.nuxtjs.dev/mountains'
      ).then((res) => res.json())
      this.mountains = mountains
      console.log(mountains)
      }catch(e){
        console.log(e)
      }
    }
}
</script>
