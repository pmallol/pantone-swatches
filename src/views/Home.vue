<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Swatches />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import Swatches from '@/components/Swatches.vue'

export default {
  name: 'Home',
  components: {
    Swatches
  }
}
</script>
