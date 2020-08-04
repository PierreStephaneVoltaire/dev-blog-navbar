<template>
  <div class="blog-navbar navbar md-layout">
    <section class=" md-layout-item navbar-section">

        <a class="home" href="/">
          <md-button class="blog-title">

          <span>Despair Driven Development</span>
          </md-button>

        </a>

    </section>
    <section class="md-layout-item navbar-section">

<!--      <md-field class="search">-->
<!--        <md-icon mdPrefix>search</md-icon>-->
<!--        <md-input class="md-small-size-100"/>-->
<!--      </md-field>-->
    </section>
    <section class="md-layout-item navbar-section blog-avatar">

      <md-menu md-direction="bottom-start">
        <md-button md-menu-trigger class="md-icon-button md-raised">
          <md-icon>person</md-icon>
        </md-button>
        <md-menu-content>
          <md-menu-item>
            <md-button @click="showDialog=!showDialog">
              <md-icon>person</md-icon>
              <span class="md-button-c-content">Sign in</span>
            </md-button>
          </md-menu-item>

<!--          <md-menu-item>-->
<!--            <md-button>-->

<!--              <md-icon>lock</md-icon>-->
<!--              <span class="md-button-c-content">Sign out</span></md-button>-->
<!--          </md-menu-item>-->
        </md-menu-content>
      </md-menu>

    </section>
    <Dialog v-bind:showDialog="showDialog"
            v-on:update:showDialog="showDialog = $event"/>

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import Dialog from '@/components/Dialog/Dialog.vue'

  @Component({
    components: { Dialog }
  })
export default class Navbar extends Vue {
    showDialog=false
    triggerNotImplemented=() => {
      alert("the User sign in/up feature hasn't been implemented yet")
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.md-button-c-content{
  padding-left: 10px !important;
}
.blog-navbar {
  background: linear-gradient(to right, white 33%,lightblue 66%,blue 85%, darkblue);
  /*width: 100vw;*/
  position: static;
  z-index: auto;
  min-height: 48px;
}
.home{
  text-decoration: none !important;
  color:black !important;
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
