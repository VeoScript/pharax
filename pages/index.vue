<template>
  <!-- Welcome Page -->
  <div class="h-screen w-full flex items-center justify-center">
    <div class="flex-row w-full text-center">
      <div class="title font-bold text-2xl text-gray-800">
        Welcome to <span class="font-extrabold text-3xl text-gray-800">Phar</span><span class="font-bold text-3xl text-yellow-400">ax</span>
      </div>
      <div class="subtitle text-sm mt-2">Your pharmacy assistant solution.</div>
      <div class="flex justify-center">
        <form @submit.prevent="pressLogin" class="mt-3 px-3 w-96">
          <div class="control-holder my-3">
            <input class="ring-4 ring-yellow-300 w-full rounded-full my-2 px-5 py-3 focus:outline-none focus:ring-yellow-400" type="text" placeholder="Email or Username">
          </div>
          <div class="control-holder my-3">
            <input class="ring-4 ring-yellow-300 w-full rounded-full px-5 py-3 focus:outline-none focus:ring-yellow-400" type="password" placeholder="Password">
          </div>
          <div class="control-holder my-3 flex-col justify-center">
            <nuxt-link class="text-sm font-medium hover:text-yellow-400" to="/">Forgot Password</nuxt-link>
            <button class="bg-yellow-300 hover:bg-yellow-400 rounded-full w-40 mt-2 ml-5 px-5 py-3 text-sm font-medium focus:outline-none" type="submit">Login</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    pressLogin() {
      this.$router.push('home')
    }
  },
}
</script>
