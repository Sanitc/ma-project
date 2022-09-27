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
          titre: ' Chambres',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
          icon: 'mdi-bed-king-outline'
        },
        {
          titre: ' Aménagement dans le gite',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
          icon: 'mdi-home-variant-outline'
        },
        {
          titre: ' Pièce commune',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
          icon: 'mdi-sofa-outline'
        },
        {
          titre: ' Cuisine',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
          icon: 'mdi-silverware-fork-knife'
        },
        {
          titre: ' Espace Spa',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
          icon: 'mdi-hot-tub'
        },
        {
          titre: ' Autour du gîte',
          github: 'https://github.com/Sanitc/phoikos',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, ",
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