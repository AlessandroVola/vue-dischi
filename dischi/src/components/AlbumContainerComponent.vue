<template>
    <div class="row">
        <div v-for="album in albums" :key="album.id" class="av-fifth-col"></div>
    </div>
</template>

<script>
export default{
    name:'AlbumContainerComponent',
    props:{
       albums : Array
    }
}
</script>

<style lang="scss" scoped>
.av-fifth-col{
    width: calc(100% / 5);
}
</style>