<template>
  <v-app>
    <v-main>
      <Links />
    </v-main>
  </v-app>
</template>

<script>
import Links from "./components/Links.vue";

export default {
  name: "App",

  components: {
    Links,
  },

  data: () => ({
    //
  }),
};
</script>
