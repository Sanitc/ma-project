<template>
  <section id="prestation" class="prestation-section">
    
     <v-container>
     <h2 class="prestation-title">Toutes les commodités pour un séjour idyllique</h2>
      <div>
        <v-row>
          <v-col sm="9" class=" card">
            <v-row class="justify-space-around mb-8 mt-4">
              <v-card
               v-for="prestation in prestations"
                :key="prestation.title"
                class="cards"
                max-width="400"
                
                
              >          
              <v-icon x-large color="brown" class="icon">{{ prestation.icon }}</v-icon>
                <v-card-title class="card-title">{{ prestation.titre }}</v-card-title>
                <v-card-text>
                  {{ prestation.description }}
                </v-card-text>
              </v-card>
            </v-row>              
          </v-col>
        </v-row>
      </div>
      
    </v-container>
  </section>
</template>

<style scoped>

</style>

<style scoped>
.icon{
  padding-top: 10px;
}

.prestation-title{
  text-align: center;
  margin-bottom: 2%;
}


.card-title{
  display: block;
    margin-left: auto;
    margin-right: auto ;
}
.card{
  display: block;
    margin-left: auto;
    margin-right: auto ;
    
}

.cards{
  border-radius: 15px;
  box-shadow: 10px 5px 5px #ADAFBC;
  text-align: center;
  margin-bottom: 2%;
}
</style>

<script>
export default {
   props: ['titre','description','icon','github'],
 data() {
    return {
      prestations: [
      {
          titre: ' Aménagement dans le gite',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Wifi et Réseau 4G. Parking pour 3 voitures, jardin cloturé de 700m2 avec jacuzzi. Préau  avec salon de jardin et possibilité chauffage l'hiver, terrasse avec table extérieure, plancha et barbecue. Mise à disposition de 4 vélos toute taille",
          icon: 'mdi-home-variant-outline'
        },
        {
          titre: ' Chambres',
          github: 'https://github.com/Sanitc/phoikos',
          description: "3 chambres doubles et un dortoir de 3 lits simples, 2 salles de bains dont une avec facilitation mobilité réduite, 1 drap de bain et une serviette de bain fournit par personnes, Linge de lit fourni",
          icon: 'mdi-bed-king-outline'
        },
        {
          titre: ' Pièce commune',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Grande table, Table de jeux,  Canapé d'angle avec TV, Mézzanine espace de lecture",
          icon: 'mdi-sofa-outline'
        },
        {
          titre: ' Cuisine',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Cuisine toute équipé avec Micro-onde, Four, Plaques induction, Lave vaisselle, Réfrigérateur, Arrière cuisine avec lave linge et sèche linge",
          icon: 'mdi-silverware-fork-knife'
        },
        {
          titre: ' Espace Spa',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Jacuzzi 5 places dont 1 allongée, douche extérieure",
          icon: 'mdi-hot-tub'
        },
        {
          titre: ' Autour du gîte',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Randonnée, marche nordique, Course a pied, VTT, Base de loisir avec canöe-kayak, paddle, escalade, tir a l'arc. Au pied de la rivière 'Le Couesnon', pêche, à 30 minutes de la mer (St Malo, Cancale, Mt St Michel)",
          icon: 'mdi-compass-outline'
        }           
      ]
    }
  },
  methods: {
    truncate(str) {
      if (str.length > 145) {
        return str.slice(0, 79) + '...'
      }
      return str
    }
  }  
}
</script>