<template>
  <div id="app">
    <header>
        <h3>Subreddits created by <a  target="_blank" href="https://github.com/ChamkhiAnas">@chamkhiAnas</a></h3>
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
      cats:["art","sports","space","movies","funny","food"]
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
  color:inherit;
}
header{
  background:#ff7979;
  color:#ffffff;
  padding:10px;
  text-align:center;
}
</style>
