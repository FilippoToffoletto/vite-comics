<script>
export default {
    name:'ComicCard',
    props:{
        card:Object
    },
}
</script>

<template>
    <div class="card">
        <div class="img">
            <img :src="card.thumb" :key="index" alt="{{card.series}}">
        </div>
        <h4>{{card.series}}</h4>
    </div>
    

  
</template>



<style lang="scss" scoped>

.card{
    padding: 10px 0px;
    padding-right: 20px;
    display: inline-block;
    flex-direction: column;
    flex-wrap: wrap;
    width: calc(100% / 6);

    h4{
        color: white;
        font-size: .9rem;
        padding: 15px 0px;
    }
    .img{
        width: 185px;
        height: 185px;
        overflow: hidden;
        img{
            object-fit: cover;
        }
    }
}


</style>