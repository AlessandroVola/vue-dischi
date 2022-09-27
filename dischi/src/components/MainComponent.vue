<template>
    <main>
        <div class="container">
            <AlbumContainerComponent :albums='album'/>
        </div>
    </main>  
</template>

<script>
import AlbumContainerComponent from './AlbumContainerComponent.vue';
import axios from 'axios';



export default{
    name:'MainComponent',
    components:{ AlbumContainerComponent},
    data(){
        return{
            apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
            albums:[]
        }
    },
    created(){
        this.getAlbumData();
    },
    methods:{
        getAlbumData(){
            axios.get(this.apiUrl)
                .then((response)=>{
               if(this.isResponseOk(response)){
                    this.albums = response.data.response;
               }
        })
        .catch((e)=>{
            console.log(e)
        })
        },
        isResponseOk({status}){
            return status===200;
        }
    }
}

</script>


<style lang="scss" scoped>
.main{
    background-color: #1e2d3b;
}

</style>

