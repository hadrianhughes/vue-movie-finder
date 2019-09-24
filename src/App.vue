<template>
  <div>
    <Layout
      siteHeading="Vue Movie Finder"
      siteSubheading="Search for a movie">
      <p>Hello World</p>
    </Layout>
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

<style>
html, body {
  font-family: sans-serif;
  margin: 0;
  text-align: center;
}
</style>
