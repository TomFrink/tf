<template>
  <v-container grid-list-xl>
    <h1 class="display-2">Welcome {{ person }}!</h1>

    <v-layout row align-center justify-space-around>
      <v-flex md3>
        <v-card dark tile flat>
          <label pt-2>What's your name?</label>
          <v-text-field
            pb-2
            pl-4
            pr-4
            v-model="person"
            label="Name"
            outlined
          ></v-text-field>
        </v-card>
      </v-flex>
    </v-layout>
    <v-layout row align-center justify-space-around>
      <v-flex md8>
        <v-card>
          <v-card-text title
            >Well, {{ person }}, my name is Tom Frink. <br />Thank you for
            coming to see my page.</v-card-text
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
