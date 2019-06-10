<template>
  <v-container>
    <v-layout>
      <v-flex>
        <div class="title mb-1 hello">{{ msg }}</div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 5px 0 0;
}
</style>
