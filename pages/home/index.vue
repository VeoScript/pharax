<template>
  <div class="h-screen">
    <Sidebar />
    <div class="flex ml-36 pt-8">
      <div class="card shadow-lg flex w-2/4 bg-yellow-500 px-10 py-5 rounded-full">
        <div class="flex-auto text-white">
          <div class="text-4xl font-medium">Hello, Jerome!</div>
          <div class="mt-2">Welcome back to Pharax</div>
        </div>
        <div class="clock flex items-center">
          <div class="time text-5xl font-bold text-gray-800">03:33 PM</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from '~/components/layouts/Sidebar'
export default {
  components: {
    Sidebar,
  },
}
</script>
