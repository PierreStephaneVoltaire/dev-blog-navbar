<template>
  <div id="app">
    <NavBar/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import NavBar from './components/Navbar.vue'

  @Component({
    components: {
      NavBar
    }
  })
export default class App extends Vue {
}
</script>

<style lang="scss">
  @import "~vue-material/dist/theme/engine"; // Import the theme engine
  @include md-register-theme("default", (
    primary: #5050ba, // The primary color of your application
  theme: light // This can be dark or light

  ));
  .md-dialog-container{
    max-height: 100% !important;
  }
  @import "~vue-material/dist/theme/all"; // Apply the theme

  .layout{
    display: flex;
  }
  .layout-row{
    flex-direction: row;
  }
  .layout-col{
    flex-direction: column;
  }

  .md-dialog-container{
    border-radius: 4px;
    border-top-color:#5050ba ;
    border-top-width: 32px;
    border-top-style: solid;
  }
  .full{
    width: 100% !important;
  }
</style>
