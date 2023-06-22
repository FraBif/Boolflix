<script>

import FilmsList from './FilmsList.vue'
import SearchBar from './SearchBar.vue'
import axios, { Axios } from 'axios'

export default{
    name:'MainApp',
    components: {
        FilmsList,
        SearchBar
    },

    data(){
        return{

            apiUrl: 'https://api.themoviedb.org/3/movie/550',
            moviesList: [],

        }
    },

    methods: {

        getMovies(searchedFilm){
        axios.get(this.apiUrl, {

        params: {

        api_key: 'ec5361fd57151ccd4ed9c4fd3683a2c2',
        query: searchedFilm
    }})
        .then( (response) => {
        console.log(response.data);
        this.moviesList= response.data;
    })
        .catch(function (error) {
        console.log(error);
    })

}

},

}

</script>


<template>

    <main>
        <SearchBar @searched="getMovies" />
        <FilmsList :movies="moviesList" />

    </main>


</template>

<style scoped>
main{
    height:100%;
    width:100%;
    color:white;
    background-color: #434343;
    
}

</style>