<template>
  <div>
    <Nuxt />
  </div>
</template>

<script>
export default {
  head: {
    link: [
      {
        rel: 'stylesheet',
        href: "https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap"
      }
    ]
  }
}
</script>

<style>
body {
  font-family: 'Inter', sans-serif;
}
body {
  @apply subpixel-antialiased;
}
</style>
