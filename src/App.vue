<template>
  <v-app>
    <v-app-bar app color="white" light>
      <v-img
        alt="Dewy Hive Logo"
        class="shrink mr-2"
        contain
        src="/img/DewyHive(4).png"
        transition="scale-transition"
        width="40"
      />
      <v-toolbar-title class="hidden-sm-and-down font-weight-black font-italic">
  DewyHive
</v-toolbar-title>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>
