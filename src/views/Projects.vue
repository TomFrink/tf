<template>
  <v-container>
    <HelloWorld msg="Welcome to Tom Frink's Playground" />
    <h2>Vanilla JavaScript</h2>
    <codepen :options="codepenInput" />
    <h2>Vue JS</h2>
    <iframe
      src="https://codesandbox.io/embed/calcy-stuyd?fontsize=14"
      title="Calcy"
      allow="geolocation; microphone; camera; midi; vr; accelerometer; gyroscope; payment; ambient-light-sensor; encrypted-media; usb"
      style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
      sandbox="allow-modals allow-forms allow-popups allow-scripts allow-same-origin"
    ></iframe>
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
        "data-height": "450",
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

<style scoped></style>
