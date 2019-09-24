<template>
  <div>
    <input
      class="Input"
      type="text"
      placeholder="Search for a movie..."
      v-on:input="onChange"
      :value="value" />
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

<style>
.Input {
  border: 1px solid #d8d8d8;
  border-radius: 5px;
  font-size: 16px;
  padding: 10px;
  width: 500px;
}
</style>
