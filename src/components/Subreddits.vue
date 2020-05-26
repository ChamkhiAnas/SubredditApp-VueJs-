<template>
    <div class="subreddit">
    <a :href="makeURL(item.data.permalink)" :style="makeImage(item.data.thumbnail)" target="_blank" class="thumbnail"></a>
    <div class="details">
        <a :href="makeURL(item.data.permalink)" :title="item.data.title" target="_blank" class="title">
                {{item.data.title}}
        </a>
        <br/>
        <div class="stats">

            <i class="material-icons">thumb_up_alt</i>
            {{item.data.score}}
            <i class="material-icons">rate_review</i>
            {{item.data.num_comments}}

        </div>
    </div>
    </div>
</template>>

<script>
export default {

        name:"subreddits",
        props:['item'],
        data(){
            return{

            }
        },
        methods:{
            makeURL:function(lnk){

                return 'http://reddit.com/'+lnk;

            },
            makeImage:function(img){
                return 'background-image:url('+img+')';

            }
        },

}
</script>>

<style scoped>

.subreddit{
    display:flex;
}
.thumbnail{
    display:block;
    flex:0 0 65px;
    height:65px;
    background-repeat:no-repeat;
    background-size:cover;
    background-position:center;
    margin-right:12px;
    border-radius:5px;
}
.subreddit .details .title{
    font-size:15px;
    margin-bottom:5px;
    color:steelblue;
}
.subreddit .stats{
    font-size:12px;
    margin-right:4px;
    margin-top:7px;
    display:inline-block;
    color:#666666
}
.subreddit .stats i{
    font-size:10px;
    margin-right:2px;
}
</style>