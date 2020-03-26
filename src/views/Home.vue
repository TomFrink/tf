<template>
  <v-container>
    <h1 class="display-2">Welcome {{ person }}!</h1>

    <v-layout align-center>
      <v-flex xs12 md6 offset-md3>
        <v-card>
          <label class="col-sm-6">What's your name?</label>
          <v-text-field v-model="person" label="Name" outlined></v-text-field>
          <v-card-text title
            >Well, {{ person }}, thank you for coming to see my
            page.</v-card-text
          >
          <p>
            There isn't a lot of stuff here at the moment. <br />
            But I promise you, there is more to come.
          </p>
          <p>
            See, I've been doing a bit of mise en place. And now it's time to
            start cooking 😊
          </p>
          <p>
            Feel free to send some feedback my way, good, bad or indifferent.
          </p>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      person: "Friend"
    };
  }
};
</script>
