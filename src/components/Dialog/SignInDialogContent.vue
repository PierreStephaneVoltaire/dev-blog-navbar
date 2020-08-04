<template>
  <div >
    <form novalidate class="layout layout-col" >
      <md-field>
        <label>Email</label>
        <md-input type="email"></md-input>
      </md-field>
      <md-field md-clearable>
        <label>Password</label>
        <md-input type="password" ></md-input>
      </md-field>
      <md-button @click="notImplemented" class="md-primary full"> sign in</md-button>
    </form>

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component({
  })
export default class SignInDialogContent extends Vue {
  notImplemented=() => {
    alert('the signin feature hasn\'t been implemented yet')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
