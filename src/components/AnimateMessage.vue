<template>
  <div class="message">
    <p>
      {{ message }}
    </p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'AnimageMessage',
  props: {
    message: String,
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.message {
  color: white;
}
</style>
