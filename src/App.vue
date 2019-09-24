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

   export default {
     name: 'App',
     components: {
       Layout,
       Input
     },
     methods: {
       changeInput: function(e) {
         this.input = e.target.value;
       }
     },
     data: () => ({
       input: ''
     })
   };
 </script>

<style>
html, body {
  font-family: sans-serif;
  margin: 0;
  text-align: center;
}
</style>
