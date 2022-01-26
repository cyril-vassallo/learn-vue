<template>
  <main>
    <h1 class="text-5xl p-5 text-gray-900" >
      Wolrd Mountains
    </h1>
    <CardsList/>
  </main>
</template>

<script>
  export default {
    name: 'Mountain',
    head() {
      return {
        title: 'learn-vue',
        meta: [
          {
            hid: 'description',
            name: 'description',
            description: 'Learn about vue by Nuxt'
          }
        ]
      }
    },
  }
</script>
