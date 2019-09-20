<template>
  <v-container>
    <HelloWorld msg="Welcome to Tom Frink's App" />
    <codepen :options="codepenInput" />
  </v-container>
</template>

<script>
import HelloWorld from "../components/HelloWorld";
import Codepen from "../components/Pen";

export default {
  name: "home",
  components: {
    HelloWorld,
    Codepen
  },
  data() {
    return {
      codepenInput: {
        "data-height": "100%",
        "data-theme-id": "dark",
        "data-slug-hash": "wLqEPe",
        "data-default-tab": "result",
        "data-user": "TFcuse",
        "data-embed-version": 2,
        "data-pen-title": "Bridge-ECL.2",
        placeholder: `
          See the Pen <a href="https://codepen.io/TFcuse/pen/wLqEPe">here</a>.
          `,
        wrapperClass: "codepen-embed"
      }
    };
  }
};
</script>
