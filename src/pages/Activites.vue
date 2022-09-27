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
          name: 'act1',
          description: "Cette application permettra de retrouver des magasins éco-responsable dans Rennes, et donnera des conseils afin de reduire son impact écologique.",
          image: 'https://raw.githubusercontent.com/Sanitc/phoikos/master/assets/images/logo/%C3%A9t%C3%A9.png'
        },
        {
          name: 'act2',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act3',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act4',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act5',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act6',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act7',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act8',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act9',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act10',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act11',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
        },
        {
          name: 'act12',
          description: "cette app...",
          image: 'https://raw.githubusercontent.com/Sanitc/website/main/src/assets/img/projet/portefolio-projet.png'
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