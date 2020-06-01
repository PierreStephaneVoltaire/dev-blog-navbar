<template>
  <md-dialog :md-active.sync="showDialog">
    <md-tabs md-dynamic-height>
      <md-tab md-label="sign in">
        <form novalidate class="md-layout" @submit.prevent="validateUser">
              <div class="md-layout md-gutter">
                <div class="md-layout-item md-large-size-100">
                  <md-field>
                    <label>Username</label>
                    <md-input ></md-input>
                  </md-field>
                </div>
                <div class="md-layout-item md-large-size-100">
                  <md-field md-clearable>
                    <label>Password</label>
                    <md-input type="password" ></md-input>
                  </md-field>
                </div>
              </div>
          <div class="md-layout-item md-large-size-100">
          <md-button class="md-primary"> sign in</md-button>
          </div>
        </form>
        </md-tab>

      <md-tab md-label="sign up">
        <md-steppers :md-active-step.sync="active" md-linear>
          <md-step id="first" md-label="Create an account" :md-editable="false"  :md-done.sync="first">
            <form novalidate class="md-layout" @submit.prevent="validateUser">
              <div class="md-layout md-gutter">
                <div class="md-layout-item md-large-size-100">
                  <md-field>
                    <label>Email</label>
                    <md-input type="email"></md-input>
                  </md-field>
                </div>
                <div class="md-layout-item md-large-size-100">
                  <md-field>
                    <label>Username</label>
                    <md-input ></md-input>
                  </md-field>
                </div>
                <div class="md-layout-item md-large-size-100">
                  <md-field md-clearable>
                    <label>Password</label>
                    <md-input type="password" ></md-input>
                  </md-field>
                </div>
              </div>
              <div class="md-layout-item md-large-size-100">
                <md-button class="md-primary"> sign in</md-button>
              </div>
            </form>

          </md-step>
          <md-step id="second" md-label="enter confirmation code" md-description="Check your email for the confirmation code" :md-editable="true"  :md-done.sync="second">
            <form novalidate class="md-layout" @submit.prevent="validateUser">
              <div class="md-layout md-gutter">
                <div class="md-layout-item md-large-size-100">
                  <md-field>
                    <label>Confirmation code</label>
                    <md-input type="number"></md-input>
                  </md-field>
                </div>
              </div>
              <div class="md-layout-item md-large-size-100">
                <md-button class="md-primary"> Confirm</md-button>
              </div>
            </form>

          </md-step>
          <md-step id="third" md-label="Create a profile" :md-editable="true"  :md-done.sync="third">
            <form novalidate class="md-layout" @submit.prevent="validateUser">
              <div class="md-layout md-gutter">
                <div class="md-layout-item md-large-size-100">
                  <md-field>
                    <label>I'm a</label>
                    <md-input type="number"></md-input>
                  </md-field>
                </div>
              </div>
              <div class="md-layout-item md-large-size-100">
                <md-button class="md-primary"> Confirm</md-button>
              </div>
            </form>

          </md-step>
        </md-steppers>

      </md-tab>
      <md-tab md-label="Forgot Password">
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam mollitia dolorum dolores quae commodi impedit possimus qui, atque at voluptates cupiditate. Neque quae culpa suscipit praesentium inventore ducimus ipsa aut.</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam mollitia dolorum dolores quae commodi impedit possimus qui, atque at voluptates cupiditate. Neque quae culpa suscipit praesentium inventore ducimus ipsa aut.</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam mollitia dolorum dolores quae commodi impedit possimus qui, atque at voluptates cupiditate. Neque quae culpa suscipit praesentium inventore ducimus ipsa aut.</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam mollitia dolorum dolores quae commodi impedit possimus qui, atque at voluptates cupiditate. Neque quae culpa suscipit praesentium inventore ducimus ipsa aut.</p>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ullam mollitia dolorum dolores quae commodi impedit possimus qui, atque at voluptates cupiditate. Neque quae culpa suscipit praesentium inventore ducimus ipsa aut.</p>
      </md-tab>

    </md-tabs>
  </md-dialog>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component
export default class Dialog extends Vue {
    private showDialog= true
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
