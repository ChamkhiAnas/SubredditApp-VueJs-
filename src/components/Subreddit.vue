<template>

    <div class="subreddits container">

        <h2>{{category | maj}}</h2>
         <ul class="item-list">
              <li v-for='(post,indx) in subreddits' :key="indx">
            <subreddits :item="post"></subreddits>
              </li>
        </ul>

    </div>

</template>



<script>
import Subreddits from './Subreddits'

export default {

    name:"Subreddit",
    props:['category'],
    data(){
        return{

            subreddits:[
            ],

        }
    },
    components: {
        Subreddits
    },
    filters:{
        maj:function(value){
            if (!value)  return '';
            value=value.toString();
            return value.charAt(0).toUpperCase()+value.slice(1);
        }
    },
    created:function(){
        this.$http.get('https://www.reddit.com/r/'+this.category+'/top.json?limit=5')
        .then((res)=>{
            this.subreddits=res.data.data.children
            console.log(this.subreddits[0].data.permalink)
        })
        ;
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