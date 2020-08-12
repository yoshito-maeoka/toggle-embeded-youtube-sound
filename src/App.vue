<template>
  <div id="app">
    <AnimatedMessage :message="message" />
    <SoundIcon :muted="muted" @clicked="onClick" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import AnimatedMessage from './components/AnimateMessage.vue';
import SoundIcon from './components/SoundIcon.vue';

export default Vue.extend({
  name: 'app',
  components: {
    AnimatedMessage,
    SoundIcon,
  },
  props: {
    targetId: {
      type: String,
    },
  },
  data() {
    return {
      message: 'please click this icon to unmute ->',
      muted: true,
    };
  },
  methods: {
    onClick() {
      this.muted = !this.muted;
      console.log('clicked emitted', this.muted);
    },
  },
});
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
