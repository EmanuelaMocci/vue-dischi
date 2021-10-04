<template>
    <div class="disco">
        <div class="img-container">
            <img src='https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg' alt="">
            <div class="text">
                <h3>NEW JERSEY</h3>
                <div>Bon Jovi</div>
                <div>1988</div>
            </div>
        </div>
    </div>
        
</template>

<script>
export default {
    name: "Disco"
    // props: {
    //     info: object
    // }
    
}
</script>

<style lang="scss" scoped>
.disco{
    display: flex;
    justify-content: center;

    .img-container{
        background-color: #2E3A46;
        width: 180px;
        margin-top: 30px;
        
        img{
        width: 140px;
        margin: 15px auto;
        display: flex;
        align-items: center;
        }
        .text{
            text-align: center;
            padding-bottom: 60px;
            h3{
                padding-bottom: 15px;
                color: white;
            }
            div{
                color: grey;
            }
        }
    }
}

</style>