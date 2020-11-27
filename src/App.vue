<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld :msg="hello" />
</template>

<script setup="props" lang="ts">
import { defineComponent, defineProps } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

export default defineComponent({
  name: "App",
  components: {
    HelloWorld
  },
  props: {
    test: {
      type: String,
      required: true,
    }
  },
  setup(props) {
    const hello: string = props.test;

    return {
      hello
    }
  }
});


</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
