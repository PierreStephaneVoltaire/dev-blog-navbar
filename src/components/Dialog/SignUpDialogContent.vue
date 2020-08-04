<template>
  <md-steppers :md-active-step.sync="active" :md-dynamic-height="true"
               :md-linear="true" md-vertical  >
    <md-step id="first" md-label="Create an account" :md-editable="false"  :md-done.sync="firstStep"  >
      <form novalidate class="layout layout-col" >
            <md-field>
              <label>Email</label>
              <md-input type="email"></md-input>
            </md-field>
            <md-field>
              <label>Username</label>
              <md-input ></md-input>
            </md-field>
            <md-field md-clearable>
              <label>Password</label>
              <md-input type="password" ></md-input>
            </md-field>
            <md-field md-clearable>
              <label> Confirm Password</label>
              <md-input type="password" ></md-input>
            </md-field>
          <md-button @click="completeFirstStep" class="md-primary full"> sign up</md-button>
      </form>

    </md-step>
    <md-step id="second" md-label="Enter confirmation code" :md-editable="false"  :md-done.sync="secondStep" md-description="Check your email for the confirmation code"  >
      <form novalidate class="layout layout-col" >
            <md-field>
              <label>Confirmation code</label>
              <md-input type="text"></md-input>
            </md-field>
          <md-button class="md-primary full" @click="completeSecondStep"> Confirm</md-button>
      </form>
    </md-step>
    <md-step id="third" md-label="Create a profile" :md-editable="false"   :md-done.sync="thirdStep"  >
      <form novalidate class="layout layout-col" >
            <md-field>
              <label>I'm a</label>
              <md-select >
                <md-option value="FrontEnd">Frontend Developer</md-option>
                <md-option value="BackEnd">Backend Developer</md-option>
                <md-option value="FullStack">FullStack Developer</md-option>
                <md-option value="Mobile">Mobile Developer</md-option>
                <md-option value="Game">Game Developer</md-option>
                <md-option value="Student">Student</md-option>
                <md-option value="Recruiter">Recruiter</md-option>
                <md-option value="Hobbyist">Hobbyist</md-option>
              </md-select>
            </md-field>
            <md-field>
              <label>About Me</label>
              <md-textarea>
              </md-textarea>
            </md-field>
          <md-field>
            <label>Resume</label>
            <md-file>

            </md-file>
          </md-field>

        <md-chips class="md-primary" v-model="this.socialChips" md-placeholder="Add a url..." md-check-duplicated>
          <div class="md-helper-text">My Social Websites and portfolios</div>
        </md-chips>

          <md-chips class="md-primary" v-model="SkillChips" md-placeholder="Add a language, framework,library or skill..." md-check-duplicated>
            <div class="md-helper-text">Skills and expertise</div>
          </md-chips>

          <md-button  class="md-primary" @click="completeThirdStep"> Confirm</md-button>

      </form>

    </md-step>
  </md-steppers>

</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

  @Component({
  })
export default class SignUpDialogContent extends Vue {
  socialChips: string[]=[]
    SkillChips: string[]=[]
firstStep=false
    active='first'
    completeFirstStep () {
      this.firstStep = true
      this.active = 'second'
    }

    secondStep=false
    completeSecondStep () {
      this.secondStep = true
      this.active = 'third'
    }

    thirdStep=false
    completeThirdStep () {
      this.secondStep = true
      alert("the sign in and profile features haven't been implemented yet")
    }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
