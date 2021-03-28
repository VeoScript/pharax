<template>
  <div class="h-screen fixed">
    <div class="w-28 text-center py-10 border-r-4 border-yellow-600 bg-yellow-300">
      <div class="title">
        <span class="font-black text-2xl text-gray-800">Phar</span><span class="font-black text-2xl text-yellow-600">ax</span>
      </div>
      <div>
        <div class="links my-14 flex justify-center" v-for="(link, i) in links" :key="i">
          <nuxt-link class="transition duration-700 ease-in-out transform hover:rotate-45" :class="$route.path === link.goto ? 'rounded-xl transition duration-700 ease-in-out transform -translate-y-3 origin-center rotate-45' : 'bg-none'" :to="link.goto">
            <span :class="$route.path === link.goto ? 'text-yellow-800' : 'text-yellow-600'" v-html="link.icon"></span>
          </nuxt-link>
          <div class="relative">
            <div class="absolute bottom-0 right-0 -mb-5 -mr-3">
              <span class="bg-gray-900 transition duration-700 ease-in-out rounded-full text-white text-xs px-2 py-1" :class="$route.path === link.goto ? 'block' : 'hidden'">{{link.title}}</span>
            </div>
          </div>
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
          icon: '<svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>',
          goto: '/home'
        },
        {
          title: 'Medicines',
          icon: '<svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>',
          goto: '/medicines'
        },
        {
          title: 'Masterfiles',
          icon: '<svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-6l-2-2H5a2 2 0 00-2 2z"></path></svg>',
          goto: '/masterfiles'
        },
        {
          title: 'Invoice',
          icon: '<svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2"></path></svg>',
          goto: '/invoice'
        },
        {
          title: 'Search',
          icon: '<svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg>',
          goto: '/search'
        }
      ]
    }
  }
}
</script>
