<script>
import Heading from "../components/about/Heading";
import LinkList from "../components/about/LinkList";

export default {
  components: {
    Heading,
    LinkList
  }
};
</script>

<template>
  <main>
    <Heading />
    <v-container grid-list-xl>
      <v-layout wrap>
        <v-flex xs12 md4>
          <LinkList />
        </v-flex>
      </v-layout>
    </v-container>
  </main>
</template>
