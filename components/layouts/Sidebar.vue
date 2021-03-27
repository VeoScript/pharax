<template>
  <div class="h-screen fixed">
    <div class="w-28 text-center py-10 border-r-2 border-gray-600 bg-yellow-300">
      <div class="title">
        <span class="font-black text-2xl text-gray-800">Phar</span><span class="font-black text-2xl text-yellow-600">ax</span>
      </div>
      <div class="links my-14 flex justify-center" v-for="(link, i) in links" :key="i">
        <div>
          <nuxt-link to="/home">
            <span class="icons mb-10" v-html="link.icon"></span>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        {
          title: 'Dashboard',
          icon: '<svg class="w-12 h-12 fill-current text-yellow-600 transform hover:rotate-45 hover:text-yellow-800" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M7 3a1 1 0 000 2h6a1 1 0 100-2H7zM4 7a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zM2 11a2 2 0 012-2h12a2 2 0 012 2v4a2 2 0 01-2 2H4a2 2 0 01-2-2v-4z"></path></svg>',
          goto: '/home'
        },
        {
          title: 'Medicine',
          icon: '<svg class="w-12 h-12 fill-current text-yellow-600 transform hover:rotate-45 hover:text-yellow-800" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z" clip-rule="evenodd"></path></svg>',
          goto: '/home'
        },
        {
          title: 'Masterfiles',
          icon: '<svg class="w-12 h-12 fill-current text-yellow-600 transform hover:rotate-45 hover:text-yellow-800" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2 6a2 2 0 012-2h5l2 2h5a2 2 0 012 2v6a2 2 0 01-2 2H4a2 2 0 01-2-2V6z"></path></svg>',
          goto: '/home'
        },
        {
          title: 'Invoice',
          icon: '<svg class="w-12 h-12 fill-current text-yellow-600 transform hover:rotate-45 hover:text-yellow-800" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M8 3a1 1 0 011-1h2a1 1 0 110 2H9a1 1 0 01-1-1z"></path><path d="M6 3a2 2 0 00-2 2v11a2 2 0 002 2h8a2 2 0 002-2V5a2 2 0 00-2-2 3 3 0 01-3 3H9a3 3 0 01-3-3z"></path></svg>',
          goto: '/home'
        },
        {
          title: 'Search',
          icon: '<svg class="w-12 h-12 fill-current text-yellow-600 transform hover:rotate-45 hover:text-yellow-800" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path></svg>',
          goto: '/home'
        }
      ]
    }
  }
}
</script>
