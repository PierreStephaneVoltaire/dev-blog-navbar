<template>
  <md-dialog :md-active.sync="show">
    <md-tabs md-dynamic-height  >
      <md-tab md-label="sign in">
        <SignInDialogContent></SignInDialogContent>
        </md-tab>

      <md-tab md-label="sign up" >
<SignUpDialogContent></SignUpDialogContent>
      </md-tab>
      <md-tab md-label="Forgot Password" >
        <ForgotPassWordDialogContent>

        </ForgotPassWordDialogContent>
        </md-tab>

    </md-tabs>
  </md-dialog>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
import SignInDialogContent from '@/components/Dialog/SignInDialogContent.vue'
import SignUpDialogContent from '@/components/Dialog/SignUpDialogContent.vue'
import ForgotPassWordDialogContent from '@/components/Dialog/ForgotPassWordDialogContent.vue'
@Component({
  components: { ForgotPassWordDialogContent, SignUpDialogContent, SignInDialogContent }
})
export default class Dialog extends Vue {
   @Prop() showDialog=false
  dialogIsShown=true
  get show (): boolean {
    console.log(this.showDialog, this.dialogIsShown)
    return this.showDialog ? this.dialogIsShown : false
  }

  set show (value: boolean) {
    this.dialogIsShown = value
  }
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
