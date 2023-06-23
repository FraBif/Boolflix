<script>
  export default{
    name:'FilmsList',
    data(){
        return
        
    },

    props: {
        movies: Array,
    },

   
}
    

</script>

<template>
      <article v-for="movie in movies">
    
    <h4>
        {{ movie.title }}
    </h4>

    <h5>
        {{ movie.original_title }}
    </h5>

    <pre>
        {{ movie.vote_average }}
    </pre>

</article>
</template>

<style scoped>

</style>