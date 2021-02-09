<template>
  <div>jokes</div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      joke: []
    }
  },
  async created() {
    const config = {
      headers: {
        'Accept' : 'application/json'
      }
    };

    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config);

      console.log(res.data);
    } catch (err) {
      console.log(err)
    };

    
  },
  head() {
    return {
      title: 'Dad Jokes',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes'
        }
      ]
    };
  }
};
</script>

<style lang="">
  
</style>