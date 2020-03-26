<template>
  <base-card dark>
    <v-img
      class="grey"
      height="400"
      width="100%"
      :src="require('@/assets/grand-canyon.jpg')"
    >
      <v-layout fill-height align-center pa-3>
        <v-flex xs12 md7 offset-md5 align-start>
          <h1 class="display-3 font-weight-light">
            Who am I?
          </h1>
          <div class="subheading text-uppercase pl-2 mb-4">
            A person that likes to build things.
          </div>
          <v-btn color="primary" depressed round>
            Learn more
          </v-btn>
        </v-flex>
      </v-layout>
    </v-img>
  </base-card>
</template>
