<template>
    <div class="disco">
        <div class="img-container">
            <img :src="info.poster" :alt="info.title">
            <div class="text">
                <h4>{{info.title}}</h4>
                <div>{{info.author}}</div>
                <div>{{info.year}}</div>
            </div>
        </div>
    </div>
        
</template>

<script>
export default {
    name: "Disco",
    props: {
        info: Object
    },
    // props: ['info']
    
}
</script>

<style lang="scss" scoped>
.disco{
    margin-right: 25px;
    
    .img-container{
        background-color: #2E3A46;
        width: 140px;
        height: 250px;
        margin-top: 20px;
        padding-top: 15px;

        img{
        width: 110px;
        margin: auto;
        display: flex;
        align-items: center;
        }
        .text{
            text-align: center;
            padding: 15px 0 35px 0;
            h4{
                padding: 0 10px 10px 12px;
                color: white;
                text-transform: uppercase;
            }
            div{
                color: grey;
                font-size: 13px;
            }
        }
    }
}

</style>