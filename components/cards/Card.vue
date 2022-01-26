<template>
  <div class="p-4">
    <div class="rounded overflow-hidden shadow-lg mb-4 m max-w-lg skew-x-9 contrast-100">
      <div v-on:click="handleHideOnClick"  class="absolute flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
        <svg xmlns="http://www.w3.org/2000/svg" fill="currentColor"  width="24" height="24" viewBox="0 0 24 24"><path d="M12.015 7c4.751 0 8.063 3.012 9.504 4.636-1.401 1.837-4.713 5.364-9.504 5.364-4.42 0-7.93-3.536-9.478-5.407 1.493-1.647 4.817-4.593 9.478-4.593zm0-2c-7.569 0-12.015 6.551-12.015 6.551s4.835 7.449 12.015 7.449c7.733 0 11.985-7.449 11.985-7.449s-4.291-6.551-11.985-6.551zm-.015 3c-2.209 0-4 1.792-4 4 0 2.209 1.791 4 4 4s4-1.791 4-4c0-2.208-1.791-4-4-4z"/>
        </svg>
      </div>
      <img  class="w-full" :src="mountain.image"  v-bind:alt="mountain.title"/>
      <div class="px-6 py-4 pb-2 felx">
        <div class="font-bold text-xl mb-2">
          {{ mountain.title }}
        </div>
        <p class="text-gray-700 text-base">{{mountain.description}}</p>
      </div>
        <div class="px-6 py-4">
          <span class="badge mr-2">Continent: {{ mountain.continent }}</span>
          <span class="badge mr-2">Mountain: {{ mountain.title }}</span>
        </div>
      </div>
  </div>
</template>

<style lang="postcss" scoped>
.badge {
  @apply inline-block bg-gray-200 rounded-full px-3 py-1 text-sm font-semibold text-gray-700;
  &:hover {
    @apply bg-gray-300;
  }
}
</style>



<script>

export default {
  methods: {
    handleHideOnClick : function(e) {
      const card = document.querySelector('#'+this.slug)
      card.style.display = 'none'
    }
  },
  props: ['slug', "mountain"],
}
</script>




   

