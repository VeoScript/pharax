<template>
  <div class="h-screen">
    <Sidebar />
    <Headbar />
  </div>
</template>

<script>
import Sidebar from '~/components/layouts/Sidebar'
import Headbar from '~/components/layouts/Headbar'
export default {
  components: {
    Sidebar,
    Headbar
  },
}
</script>
