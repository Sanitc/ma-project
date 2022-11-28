<template>
  <v-app v-if="isMobile">
      <v-app-bar
        app
        color="brown"
        dark        
        
      >
        <v-spacer></v-spacer>

        <v-btn        
          text
          href="#accueil"
          @click="$vuetify.goTo('#accueil')"
        >
          <span class="mr-2">
            <v-icon
              large
            >
              mdi-home
            </v-icon>
          </span>
        </v-btn>

        <v-btn        
          text
          href="#gite"
        @click="$vuetify.goTo('#gite')"
        >
          <span class="mr-2">
            <v-icon
              large
            >
              mdi-domain
            </v-icon>
          </span>
        </v-btn>

        <v-btn        
          text
          href="#prestations"
          @click="$vuetify.goTo('#prestations')"
          
        >
          <span class="mr-2">
            <v-icon
              large
            >
              mdi-domain
            </v-icon>
          </span>
        </v-btn>

        <v-btn        
          text
          href="#activites"
          @click="$vuetify.goTo('#activites')"
          
        >
          <span class="mr-2">
            <v-icon
              large
            >
              mdi-compass-outline
            </v-icon>
          </span>
        </v-btn>

        <v-btn        
          text
          href="#reservation"
          @click="$vuetify.goTo('#reservation')"
          
        >
          <span class="mr-2">
            <v-icon
              large
            >
              mdi-email
            </v-icon>
          </span>
        </v-btn>
      </v-app-bar>
    

    <v-main>
      <Accueil id="accueil"/>
      <Gite id="gite"/>
      <Prestations id="prestations"/>
      <Activites id="activites"/>      
      <Reservation id="reservation"/>
     
    </v-main>
  </v-app>
  <v-app v-else>
      <v-app-bar
        app
        color="brown"
        dark        
        
      >
        <v-spacer></v-spacer>

        <v-btn        
          text
          href="#accueil"
          @click="$vuetify.goTo('#accueil')"
        >
          <span class="mr-2">Accueil</span>
        </v-btn>

        <v-btn        
          text
          href="#gite"
        @click="$vuetify.goTo('#gite')"
        >
          <span class="mr-2">Le Gîte</span>
        </v-btn>

        <v-btn        
          text
          href="#prestations"
          @click="$vuetify.goTo('#prestations')"
          
        >
          <span class="mr-2">Prestations</span>
        </v-btn>

        <v-btn        
          text
          href="#activites"
          @click="$vuetify.goTo('#activites')"
          
        >
          <span class="mr-2">Activités</span>
        </v-btn>

        <v-btn        
          text
          href="#reservation"
          @click="$vuetify.goTo('#reservation')"
          
        >
          <span class="mr-2">Réservation</span>
        </v-btn>
      </v-app-bar>
    

    <v-main>
      <Accueil id="accueil"/>
      <Gite id="gite"/>
      <Prestations id="prestations"/>
      <Activites id="activites"/>      
      <Reservation id="reservation"/>
     
    </v-main>
  </v-app>
</template>

<script>
import Accueil from './pages/Accueil';
import Gite from './pages/Gite.vue';
import Prestations from './pages/Prestations.vue';
import Activites from './pages/Activites.vue';
import Reservation from './pages/Reservation.vue';

export default {
  name: 'App',
  components: {
    Accueil,
    Gite,
    Prestations,
    Activites,
    Reservation,
  
},
computed: {
   isMobile() {
      return this.$vuetify.breakpoint.xsOnly;
   }
},
  data: () => ({
    //
  }),
};
</script>