<template>
  <div>
    <button @click="click">
      click me
    </button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop({ default: 'informme' })
    message!: string;

  click() {
    console.log('hello', this.message);
    alert(this.message);
  }
}
</script>

<style scoped>
</style>
