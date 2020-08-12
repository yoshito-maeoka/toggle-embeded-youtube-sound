<template>
  <div class="sound-icon" @click="onClick">
    <template v-if="!muted">
      on
    </template>
    <template v-else>
      off
    </template>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'SoundIcon',
  props: {
    muted: Boolean,
  },
  methods: {
    onClick() {
      this.$emit('clicked');
      console.log('icon clicked');
    },
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
