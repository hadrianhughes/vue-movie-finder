<template>
  <div>
    <h1>{{ siteHeading }}</h1>
    <p>{{ siteSubheading }}</p>
  </div>
</template>

<script>
  export default {
    name: 'Layout',
    props: {
      siteHeading: {
        type: String,
        required: true
      },
      siteSubheading: {
        type: String,
        required: false
      }
    }
  }
</script>
