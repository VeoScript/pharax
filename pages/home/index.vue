<template>
  <div class="h-screen">
    <Sidebar />
    <Headbar />
    <Pos-Machine />
  </div>
</template>

<script>
import Sidebar from '~/components/layouts/Sidebar'
import Headbar from '~/components/layouts/Headbar'
import PosMachine from '~/components/layouts/PosMachine'
export default {
  components: {
    Sidebar,
    Headbar,
    PosMachine
  },
}
</script>
