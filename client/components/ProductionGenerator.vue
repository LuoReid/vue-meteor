<template>
  <div class="production-generator">
    <h1>Measure production</h1>
    <section class="actions">
      <button v-on:click="generateMeasure(false)">Generate Measure</button>
      <button v-on:click="generateMeasure(true)">Generate Error</button>
    </section>
  </div>
</template>
<script>
import { Meteor } from "meteor/meteor";
export default {
  methods: {
    generateMeasure(error) {
      const value = Math.round(Math.random() * 100);
      const measure = { value, error };
      Meteor.call("measure.add", measure);
    }
  }
};
</script>

