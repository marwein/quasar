<template>
  <div>
    <div class="layout-padding">
      <q-toggle label="Alternative Labels" v-model="alt" />
      <br><br>

      <q-stepper :color="color" flat ref="stepper" v-model="step" :alternative-labels="alt">
        <q-step default name="first" title="Ad style">
          <div v-for="n in 10">Step 1</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper.next()">Continue</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step error name="second" title="Custom channels" subtitle="Alert message">
          <div v-for="n in 10">Step 2</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step name="third" title="Get code">
          <div v-for="n in 3">Step 3</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step name="fifth" disable title="Disabled">
          <div v-for="n in 3">Step 4</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step name="fourth" title="Editable">
          <div v-for="n in 3">Step 5</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper.goToStep('first')">Restart</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>

        <q-stepper-navigation>
          <q-btn :color="color" flat @click="$refs.stepper.previous()">Back</q-btn>
          <q-btn :color="color" @click="$refs.stepper.next()">Next</q-btn>
        </q-stepper-navigation>
      </q-stepper>

      <br><br>

      <q-stepper ref="stepper2" :color="color" v-model="step2" :alternative-labels="alt" vertical>
        <q-step default name="first" title="Ad style">
          <div v-for="n in 10">Step 1</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper2.next()">Continue</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step error title="Custom channels" subtitle="Alert message">
          <div v-for="n in 10">Step 2</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper2.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper2.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step title="Get code">
          <div v-for="n in 3">Step 3</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper2.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper2.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step name="fifth" disable title="Disabled">
          <div v-for="n in 3">Step 4</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper2.next()">Next</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper2.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
        <q-step name="fourth" title="Editable">
          <div v-for="n in 3">Step 5</div>
          <q-stepper-navigation>
            <q-btn :color="color" @click="$refs.stepper2.goToStep('first')">Restart</q-btn>
            <q-btn :color="color" flat @click="$refs.stepper2.previous()">Back</q-btn>
          </q-stepper-navigation>
        </q-step>
      </q-stepper>
    </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
      step: 'first',
      step2: 'first',
      alt: false,
      color: 'secondary',
      text: ''
    }
  }
}
</script>
