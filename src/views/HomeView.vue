<template>
  <div class="home">
    <HeroAppVue />
  </div>
</template>

<script>
// @ is an alias to /src
import HeroAppVue from '@/components/HeroApp.vue'
export default {
  name: 'HomeView',
  components: {
    HeroAppVue
  }
}
</script>
