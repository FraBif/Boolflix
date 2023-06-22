<script>

export default{
    name:'SearchBar',
    data(){
        return{
            searchedFilm: '',
        }
    }
}

</script>

<template>
    <div class="d-flex align-items-center">
        <input type="text" name="" id="" placeholder="Films Searcher" class="py-1" v-model="searchedFilm" >
        <button  @click="$emit('searched', searchedFilm)" type="button" class="btn btn-outline-primary mx-3">Find a film</button>



    </div>


</template>

<style scoped>

</style>