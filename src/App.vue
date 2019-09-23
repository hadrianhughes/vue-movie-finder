<template>
  <div>
    <Layout
      siteHeading="Vue Movie Finder"
      siteSubheading="Search for a movie" />
  </div>
</template>

 <script>
   import Layout from './components/Layout.vue';

   export default {
     name: 'App',
     components: {
       Layout
     }
   }
 </script>
