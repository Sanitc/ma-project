<template>
  <v-app>
    <v-app-bar
      app
      color="brown"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

      </div>

      <v-spacer></v-spacer>

      <v-btn        
        text
      >
        <span class="mr-2">Accueil</span>
      </v-btn>

      <v-btn        
        text
      >
        <span class="mr-2">Le Gîte</span>
      </v-btn>

      <v-btn        
        text
      >
        <span class="mr-2">Prestations</span>
      </v-btn>

      <v-btn        
        text
      >
        <span class="mr-2">Activités</span>
      </v-btn>

      <v-btn        
        text
      >
        <span class="mr-2">Réservation</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Accueil/>
      <Gite/>
      <Prestations/>
      <Reservation/>
    </v-main>
  </v-app>
</template>

<script>
import Accueil from './pages/Accueil';
import Gite from './pages/Gite.vue';
import Prestations from './pages/Prestations.vue';
import Reservation from './pages/Reservation.vue';
export default {
  name: 'App',
  components: {
    Accueil,
    Gite,
    Prestations,
    Reservation
},
  data: () => ({
    //
  }),
};
</script>