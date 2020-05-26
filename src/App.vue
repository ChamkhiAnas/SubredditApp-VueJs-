<template>
  <div id="app">
    <header>
        <h3>Subreddits</h3>
    </header>
        <subreddit></subreddit>

  </div>
</template>

<script>

  import Subreddit from './components/Subreddit'

export default {
  name: 'App',
  components: {

    Subreddit

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
