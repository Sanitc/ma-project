<template>
  <div id="app">
    <v-app>
        <nav>
            <v-toolbar id="toolbar" color="brown">
                <v-spacer></v-spacer>                
                    <v-icon class="hidden-md-and-up" @click="toggleMenu = !toggleMenu" color="white" >mdi-menu</v-icon>                
                <v-menu
                v-model="showMenu"
                :absolute="toggleMenu"
                :content-class="'px-2 elevation-0'"    
                min-width="100%">
                    <div class="d-flex flex-md-row justify-end" v-if="!toggleMenu" >
                        <v-btn       
                          text
                          color="white"
                          @click="$vuetify.goTo('#accueil')"
                        >
                          <span class="mr-2">Accueil</span>
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          href="#gite"
                        @click="$vuetify.goTo('#gite')"
                        >
                          <span class="mr-2">Le Gîte</span>
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          @click="$vuetify.goTo('#prestations')"
                          
                        >
                          <span class="mr-2">Prestations</span>
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          @click="$vuetify.goTo('#reservation')"
                          
                        >
                          <span class="mr-2">Réservation</span>
                        </v-btn>
                    </div>
                    <div class="" v-else >
                              <v-btn       
                          text
                          color="white"
                          @click="$vuetify.goTo('#accueil')"
                        >
                          <v-icon>mdi-home-outline</v-icon>  
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          href="#gite"
                        @click="$vuetify.goTo('#gite')"
                        >
                          <v-icon>mdi-image</v-icon>  
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          @click="$vuetify.goTo('#prestations')"
                          
                        >
                          <v-icon>mdi-pool</v-icon>  
                        </v-btn>

                        <v-btn        
                          text
                          color="white"
                          @click="$vuetify.goTo('#reservation')"
                          
                        >
                          <v-icon>mdi-ticket</v-icon>  
                        </v-btn>

                    </div>
                </v-menu>
            </v-toolbar>
        </nav>
        <v-main>
          <Accueil id="accueil"/>
          <Gite id="gite"/>
          <Prestations id="prestations"/>
          <Activites id="activites"/>      
          <Reservation id="reservation"/>
        </v-main>
    </v-app>
</div>
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
  data() {
        return {
            toggleMenu: false,
        }
    },
    computed: {
        showMenu() {
            return this.toggleMenu || this.$vuetify.breakpoint.mdAndUp
        }
    }
};
</script>

