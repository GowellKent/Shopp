<template>
  <div class="home">
      <Navbb />
      <div class="container">
        <HerBan />
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbb from '@/components/NavigationBar'
import HerBan from '@/components/HeroBanner'

export default {
  name: 'HomeView',
  components: {
    Navbb, HerBan
  }
}
</script>
