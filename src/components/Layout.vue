<template>
  <div>
    <header>
      <h1>{{ siteHeading }}</h1>
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
      }
    }
  }
</script>
