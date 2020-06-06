<template>
  <div >
  <form novalidate class="md-layout" >
        <div class="md-layout md-gutter">
          <div class="md-layout-item md-large-size-100">
            <md-field>
              <label>Username</label>
              <md-input v-model="form.username" ></md-input>
            </md-field>
          </div>
          <div class="md-layout-item md-large-size-100">
            <md-field md-clearable>
              <label>Password</label>
              <md-input v-model="form.password" type="password" ></md-input>
            </md-field>
          </div>
        </div>
        <div class="md-layout-item md-large-size-100">
          <md-button @click="signin"   class="md-primary"> sign in</md-button>
        </div>
      </form>

  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component({
  })
export default class SignInDialogContent extends Vue {
      form={
        username: '',
        password: ''
      }

  signin=() => {
    console.log(this.form)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
