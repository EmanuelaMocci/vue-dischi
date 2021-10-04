<template>
    <section class="main">
        <div class="img">
            <Disco/>
        </div>
    </section>
</template>

<script>
import Disco from './Disco.vue'

// import axios from 'axios';
export default {
    name: 'Dischi',
    components: {
        Disco
    }
    // data(){
    //     return{
    //         Dischi: []
    //     }
    // }
    // created(){
    //     axios.get("https://flynn.boolean.careers/exercises/api/array/music")
    //     .then((res) => {
    //         this.Dischi = res.data.response;
    //     });
    // }
    
}
</script>

<style lang="scss" scoped>
.main{
    background-color: #1E2D3B;
    height: calc(100vh - 69px);
}
</style>