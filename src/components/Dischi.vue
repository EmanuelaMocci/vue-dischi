<template>
    <section class="main">
        <div class="contenitore-img">
            <div class="img" v-for="(item, index) in Dischi" :key="index">
                <Disco :info="item"/>
            </div>
        </div>
    </section>
</template>

<script>
import Disco from './Disco.vue';
import axios from 'axios';

export default {
    name: 'Dischi',
    components: {
        Disco,
    },
    data(){
        return{
            Dischi: []
        }
    },
    created(){
        axios.get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
            this.Dischi = res.data.response;
        });
    }
    
}
</script>

<style lang="scss" scoped>
.main{
    background-color: #1E2D3B;
    height: calc(100vh - 69px);

    .contenitore-img{
        display: flex;
        flex-wrap: wrap;
        max-width: 60%;
        margin: auto;
        padding-top: 35px;
    }
}
</style>