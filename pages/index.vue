<template>
  <!-- Welcome Page -->
  <div class="h-screen w-full flex items-center justify-center">
    <div class="flex-row w-full text-center">
      <div class="title font-bold text-lg text-gray-800">
        Welcome to <span class="font-extrabold text-2xl text-black">Phar</span><span class="font-bold text-2xl text-yellow-400">ax</span>
      </div>
      <div class="subtitle">Your pharmacy assistant solution.</div>
      <div class="flex justify-center">
        <div class="mt-3 w-96">
          <div class="control-holder my-3">
            <input class="ring-4 ring-yellow-300 w-full rounded-full my-2 px-5 py-3 focus:outline-none focus:ring-yellow-400" type="text" placeholder="Email">
          </div>
          <div class="control-holder my-3">
            <input class="ring-4 ring-yellow-300 w-full rounded-full px-5 py-3 focus:outline-none focus:ring-yellow-400" type="password" placeholder="Password">
          </div>
          <div class="control-holder my-3 flex-col justify-center">
            <nuxt-link class="text-sm font-medium hover:text-yellow-400" to="/">Forgot Password</nuxt-link>
            <button class="bg-yellow-300 hover:bg-yellow-400 rounded-full w-40 mt-2 ml-5 px-5 py-3 text-sm font-medium focus:outline-none">Login</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>
