<template>
  <div class="card-album">
    <img class="w-100" :src="info.poster" :alt="info.title" />
    <p> {{ info.title }}</p>
  </div>
</template>

<script>


export default {
    name: 'AlbumCardComponent',
    props:{
        info: Object
    },
    methods:{
        
    }
}
</script>

<style lang="scss" scoped>
.card-album{
    display: flex;
    flex-direction: column;
    text-align: center;
    padding: 20px;
    background-color: #2e3a46;
    color: #ccc;
    height: 100%;
    p{
        color: #fff;
        text-transform: uppercase;
        margin-top: 5px;
    }
}
</style>