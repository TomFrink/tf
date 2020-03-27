<template>
  <v-container pa-0>
    <base-subheading>Relevant Links</base-subheading>
    <v-layout align-center mb-2>
      <v-flex xs12 d-flex>
        <v-img
          :src="require(`@/assets/github_icon.png`)"
          class="mr-3"
          height="36"
          max-width="36"
        />
        <div>
          <div class="subheading" align-center>
            <a href="https://github.com/TomFrink"
              ><v-img
                :src="require('@/assets/github_logo.png')"
                height="36"
                max-width="100"
            /></a>
          </div>
          <div class="caption">
            UserName: TomFrink
          </div>
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "LinkList"
};
</script>
