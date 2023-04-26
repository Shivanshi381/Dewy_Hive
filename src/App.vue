<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      light
      
    >
     <v-img
  alt="Dewy Hive Logo"
  class="shrink mr-2"
  contain
  src="/img/DewyHive(4).png"
  transition="scale-transition"
  width="40"
/>


<v-img
  alt="DewyHive Name"
  class="shrink mt-1 hidden-sm-and-down"
  contain
  min-width="100"
  src="/img/name.jpg"
  width="100"
  style="margin-top: -10px"
/>

      </div>

      <v-spacer></v-spacer>

      
    </v-app-bar>

    <v-main>
      <router-view/>
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
