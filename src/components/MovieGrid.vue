<template>
  <ul class="MovieGrid">
    <li v-for="movie in movies">
      {{ movie.Title }}
    </li>
  </ul>
</template>

 <script>
   export default {
     name: 'MovieGrid',
     props: {
       movies: {
         type: Array,
         required: false,
         default: []
       }
     }
   };
 </script>

<style>
.MovieGrid {
  list-style-type: none;
}
</style>
