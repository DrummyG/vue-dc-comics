<template>
    <div class="card">
        <img :src="link" :alt="type">
        <p>{{type}}</p>
    </div>
</template>

<script>
export default {
    name: 'AppCard',
    props: {
        link : String,
        type : String
    }
}
</script>

<style lang="scss" scoped>
    .card{
        width: 150px;

        img{
            width: 100%;
            height: 150px;
            object-fit: cover;
            object-position: 0% 0%;
        }

        p{
            color: white;
            text-transform: uppercase;
        }
    }
</style>