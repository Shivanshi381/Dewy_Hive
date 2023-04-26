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
      
      
      <v-toolbar-title class="hidden-sm-and-down font-weight-black font-italic" style="display: flex; align-items: center;">
        DewyHive
        
        
      </v-toolbar-title>
      <v-spacer style="flex-grow: 1;"></v-spacer> 
      <v-text-field hide-details single-line placeholder="  Search..." style="margin-right: 20px; margin-left: 40px;"></v-text-field>
        <v-btn icon><v-icon>mdi-magnify</v-icon></v-btn>
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
