
<template>
  <v-app class="bg-grey-lighten-3">
    <Navbar/>
    <!-- <Dashboard></Dashboard> -->
    <v-content>
        <RouterView></RouterView>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue';
// import Dashboard from './components/Dashboard.vue';
export default{
  name: 'AppNavbar',
  // components: { Navbar, Dashboard },
  components: { Navbar },
  data () {
    return {

    }
  }
}
</script>