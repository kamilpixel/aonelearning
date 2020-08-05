<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
    <div class="container">
      <div class="row">
        <div class="col-12">
          <b-navbar toggleable="lg" type="dark" variant="info">
            <b-navbar-brand href="/">MyLearning</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
              <b-navbar-nav class="ml-auto">
                <b-nav-item-dropdown right>
                  <template v-slot:button-content>
                    John Doe
                  </template>
                  <b-dropdown-item href="#">Profile</b-dropdown-item>
                  <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                </b-nav-item-dropdown>
              </b-navbar-nav>
            </b-collapse>
          </b-navbar>
        </div>
      </div>
    </div>
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Footer from '@/components/Footer';


export default {
  name: 'app',
  components: {
   Footer, 
  }
}
</script>

<style lang="scss">

</style>
