<template>
  <div>
    <header>
      <h1>{{ siteHeading }}</h1>
      <p>{{ siteSubheading }}</p>
    </header>
    <main>
      <slot />
    </main>
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
