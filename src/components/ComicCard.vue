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
    flex-direction: column;
    width: calc(100% / 6 - 10px);
    padding-right: 10px;
    .img{
        width: 185px;
        height: 185px;
        overflow: hidden;
        img{
            object-fit: contain;
            overflow: hidden;
            transform: scale(1.1);
        }
    }
    h4{
        color: white;
        font-size: .9rem;
        padding: 15px 0px;
    }
}


</style>