<template>
    <div class="subreddit">
    <a :href="makeURL(item.data.permalink)" :style="makeImage(item.data.thumbnail)" target="_blank" class="thumbnail"></a>
    <div class="details">
        <a :href="makeURL(item.data.permalink)" :title="item.data.title" target="_blank" class="title">
                {{item.data.title}}
        </a>
        <br/>
        <div class="stats">
            
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

</style>