<template>
  <div id="app">
    <header>
        <h3>Subreddits</h3>
    </header>
        <subreddit :category="cats[0]"></subreddit>
        <subreddit :category="cats[1]"></subreddit>
        <subreddit :category="cats[2]"></subreddit>
        <subreddit :category="cats[3]"></subreddit>
        <subreddit :category="cats[4]"></subreddit>
        <subreddit :category="cats[5]"></subreddit>

        
  </div>
</template>

<script>

  import Subreddit from './components/Subreddit'

export default {
  name: 'App',
  components: {

    Subreddit

  },
  data:function(){
    return{
      cats:["movies","sports","space","art","funny","food"]
    }
  }
}
</script>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color:#666666;
  background:#f4f4f4;
  margin:0;
  padding:0;
}
a{
  text-decoration:none;
}
header{
  background:coral;
  color:#ffffff;
  padding:10px;
  text-align:center;
}
</style>
