<template>
  <div>
    <input type="text" v-on:input="onChange" :value="value" />
  </div>
</template>

 <script>
   export default {
     name: 'Input',
     methods: {
       onChange(e) {
         this.$emit('changed', e);
       }
     },
     props: {
       value: {
         type: String,
         required: true
       }
     }
   };
 </script>
