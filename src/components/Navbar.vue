<template>
  <div class="blog-navbar navbar md-layout">
    <section class=" md-layout-item navbar-section">
      <md-button class="blog-title">

        <span>Despair Driven Development</span>

      </md-button>
    </section>
    <section class="md-layout-item navbar-section">

      <md-field class="search">
        <md-icon mdPrefix>search</md-icon>
        <md-input class="md-small-size-100"/>
      </md-field>
    </section>
    <section class="md-layout-item navbar-section blog-avatar">

      <md-menu md-direction="bottom-start">
        <md-button md-menu-trigger class="md-icon-button md-raised">
          <md-icon>home</md-icon>
        </md-button>
        <md-menu-content>
          <md-menu-item>
            <md-icon>person</md-icon>
            <span>Sign in</span></md-menu-item>
          <md-menu-item>
            <md-icon>person</md-icon>
            <span>Sign up</span></md-menu-item>
        </md-menu-content>
      </md-menu>

    </section>
    <Dialog/>

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import Dialog from '@/components/Dialog/Dialog.vue'
@Component({
  components: { Dialog }
})
export default class Navbar extends Vue {
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  .blog-navbar {
    background: white;
    /*width: 100vw;*/
    position: static;
    z-index: auto;
    min-height: 48px;
  }

  .blog-title {
    text-align: center;
    font-family: Roboto;
    font-style: italic;
    font-weight: bold;
    font-size: 15px;
    /* or 97% */

    display: flex;
    align-items: center;
    text-align: center;
    color: #000000;
  }

  .blog-avatar {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    padding-top: 0;
    height: 48px;
    padding-right: 2em;

  }

  .search {
    min-height: 0 !important;
    margin: 0 !important;
  }
</style>
