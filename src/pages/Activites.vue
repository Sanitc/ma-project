<template>
  <section id="activite" class="activite-section">  
    <v-container>
      <div class="activite-section">
        <v-row>
          <v-col sm="12" class="d-flex flex-column justify-center ">
            <div>
              <h2 class="activite-title">Activités autour du gîte</h2>
              <div class="activite-grid">
                <v-row class="justify-space-around mb-8 mt-4">
                  
                  
                    <v-card
            v-for="project in projects"
            :key="project.name"
            class="cards"
            max-width="300"
            
          >
            <v-img
              class="align-end"
              height="250px"
              :src="project.image"
            />
            <v-card-title>{{ project.name }}</v-card-title>

            <v-card-text>
              {{ truncate(project.description) }}
            </v-card-text>
          </v-card>
                    
                  
                </v-row>   
              </div>      
            </div>   
          </v-col>
        </v-row>
      </div>
      
    </v-container>
  </section>
</template>

<style scoped>

.activite-title{
  text-align: center;
}
.activite-img{
  height: 100;
  
  
}
.img-grid{
  
  height: 284px;
  width: 400px;
  
  cursor:pointer;
}

.activite-grid{
  margin-top: 2%;
}

.activite-section{
  margin-bottom: 2%;
}

.cards{
  border-radius: 20px;
}
</style>

<script>



export default {
  name: "Activite",
  data() {
    return {
      projects: [
        {
          name: 'Chateau de Fougères',
          description: "Cette application permettra de retrouver des magasins éco-responsable dans Rennes, et donnera des conseils afin de reduire son impact écologique.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act1.png'
        },
        {
          name: 'Vieux Rennes',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act2.png'
        },
        {
          name: 'Rennes',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act3.png'
        },
        {
          name: 'Gr34',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act4.png'
        },
        {
          name: 'La vallée du couesnon',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act5.png'
        },
        {
          name: "base d'activité de la méziere",
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act6.png'
        },
        {
          name: 'canöe kayak',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act7.png'
        },
        {
          name: 'escalade',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act8.png'
        },
        {
          name: 'accrobranche',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act12.png'
        },
        {
          name: 'mont Saint Michel',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act10.png'
        },
        {
          name: 'Saint Malo',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act11.png'
        },
        {
          name: 'Cancal',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act9.png'
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