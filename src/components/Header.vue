<template>
    <div class="header">
        <div class="img-header">
            <img src="../assets/img/spotify-logo.png" alt="">
        </div>

        <div class="select-header">
            <select name="Genere" id="">
                <option value="">Scegli un genere</option>
                <option value="">Rock</option>
                <option value="">Pop</option>
                <option value="">Jazz</option>
                <option value="">Metal</option>
            </select>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header'
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
    }
}
</style>
