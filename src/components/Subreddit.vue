<template>

    <div class="subreddits container">

        <h2>Food</h2>
         <ul class="item-list">
              <li v-for='(post,indx) in subreddits' :key="indx">{{post.name}}</li>
        </ul>

    </div>

</template>



<script>

export default {

    name:"Subreddit",
    props:['category'],
    data(){
        return{

            subreddits:[
                {
                name:'My Subreddit 1'
                },
                {
                name:'My Subreddit 2'
                },
                {
                name:'My Subreddit 3'
                },
            ],

        }
    }


}

</script>


<style scoped>

.container{
    max-width:600px;
    margin:30px auto;
    background-color:#ffffff;
    box-shadow:0 0 3px #95a5a6;
}

.subreddits{
    min-width:400px;
    padding:25px 45px;
}

.subreddits h2{
    font-size:20px;
    margin-bottom: 10px;
    margin-top: 0;
}

.subreddits .item-list{
    border-top: 1px solid #cccc;
    padding-top:20px;
    list-style: none;
}
.subreddits .item-list li{
margin-bottom: 20px;
}
</style>