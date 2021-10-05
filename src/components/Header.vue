<template>
    <div class="header">
        <div class="img-header">
            <img src="../assets/img/spotify-logo.png" alt="">
        </div>

        <div class="select-header">
            <select name="" v-model="genre" @change="$emit('selectGenres', genre)">
                <option value="">Scegli un genere</option>
                <option v-for="(genre, index) in genres" :key="index">{{genre}}</option>
                <!-- <option value="">Pop</option> -->
                <!-- <option value="">Jazz</option>
                <option value="">Metal</option> -->
            </select>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
    props: ['genres'],
    data() {
        return {
            genre: ""
        }
    }
}
</script>

<style lang="scss" scoped>
.header{
    background-color: #2E3A46;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .img-header{

        img{
            width: 100px;
            padding: 10px 20px;
        }
    }
    .select-header{
        padding-right: 20px;

        select{
            padding: 5px 10px;
            border-radius: 7px;
            border: 3px solid #1E2D3B;
            outline: 0px;
        }
    }
}
</style>
