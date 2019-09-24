<template>
  <div>
    <Layout
      siteHeading="Movie Finder">
      <Input @changed="changeInput" :value="input" />
    </Layout>
  </div>
</template>

 <script>
   import Layout from './components/Layout.vue';
   import Input from './components/Input.vue';

   const fetchMovies = searchTerm => new Promise((resolve, reject) => {
     fetch(`http://www.omdbapi.com/?apikey=8eff793c&s=${searchTerm}`)
      .then(response => response.json())
      .then(resolve)
      .catch(reject);
   });

   let loadMoviesTimeout;

   export default {
     name: 'App',
     components: {
       Layout,
       Input
     },
     methods: {
       changeInput(e) {
         this.input = e.target.value;
       },
       loadMovies() {
         if (this.input.length > 0) {
           fetchMovies(this.input)
             .then(result => {
               this.results = result.Search;
             });
         }
       }
     },
     data: () => ({
       input: '',
       results: []
     }),
     watch: {
       input() {
         clearTimeout(loadMoviesTimeout);
         loadMoviesTimeout = setTimeout(this.loadMovies, 500);
       }
     }
   };
 </script>

<style>
html, body {
  font-family: sans-serif;
  font-size: 16px;
  margin: 0;
  text-align: center;
}
</style>
