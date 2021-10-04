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
    display: flex;
    justify-content: center;

    .img-container{
        background-color: #2E3A46;
        width: 150px;
        height: 250px;
        margin-top: 20px;

        img{
        width: 115px;
        margin: 15px auto;
        display: flex;
        align-items: center;
        }
        .text{
            text-align: center;
            padding-bottom: 35px;
            h4{
                padding: 0 10px 0 12px;
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