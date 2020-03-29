<template>
  <v-container align-content-center pa-3>
    <v-layout mb-2>
      <v-card class="ma-3 pa-3">
        <v-img :src="require(`@/assets/github_icon.png`)" auto-height> </v-img>
        <v-card-title primary-title class="justify-center">
          <div>
            <h3 class="headline">Github</h3>
          </div>
        </v-card-title>
        <v-card-actions class="justify-center">
          <a href="https://github.com/TomFrink" target="_blank">
            <v-btn text>Visit</v-btn>
          </a>
        </v-card-actions>
      </v-card>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "LinkList"
};
</script>
