<template>
    <section class="main">
        <div class="contenitore-img">
            <div class="img">
                <Disco class="disco-img" v-for="(item, index) in dischiFiltered" :key="index" :info="item"/>
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
        Disco
    },
    props: ['selectedGenre'],
    data(){
        return{
            dischi: []
        }
    },
    created(){
        axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
            this.dischi = res.data.response;
            const genreList = [];
            this.dischi.forEach(
                (elm) => {
                    if(!genreList.includes(elm.genre)){
                        genreList.push(elm.genre);
                    }
                }
            );
            this.$emit('genreList', genreList);
        });
    },
    computed: {
        dischiFiltered() {
            const arrFiltered = this.dischi.filter(
                (elm) => {
                    if(elm.genre.toLowerCase().includes(this.selectedGenre.toLowerCase()) ) {
                        return true;
                    }
                    return false;
                }
            )
            return arrFiltered;
        }
    }
    
}
</script>

<style lang="scss" scoped>
.main{
    background-color: #1E2D3B;
    height: calc(100vh - 69px);

    .contenitore-img{
        .img{
            display: flex;
            flex-wrap: wrap;
            max-width: 60%;
            margin: auto;
            padding-top: 35px;
        }
    }
}
</style>