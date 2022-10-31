<template>
    <section id="activite" class="activites-section">
      
       <v-container>
        <h2 class="activite-title">Activités autour du gîte</h2>
        <div>
          <v-row>
            <v-col sm="9" class=" card">
              <v-row class="justify-space-around mb-8 mt-4">
                <v-card
                 v-for="project in projects"
                    :key="project.name"
                    class="cards"
                    max-width="400"
                  
                  
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
  
  .activite-title{
    text-align: center;
    margin-bottom: 2%;
  }
  
  
  .card-title{
    display: block;
      margin-left: auto;
      margin-right: auto ;
  }
  .activites-section{
    margin-bottom: 2%;
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
     
     data() {
    return {
      projects: [
        {
          name: 'Chateau de Fougères',
          description: "Découvrer la plus grande cité médiéval d'Europe, à 25 minutes du gite.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act1.png'
        },
        {
          name: 'Rennes',
          description: "La capital bretonne, vous ouvre ses portes, à une demi heure (Musée de Bretagne, Parcs, Gastronomie, architecture, vieux Rennes...).",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act2.png'
        },
        {
          name: 'Gr39',
          description: "Randonnée sur le GR39 à travers la Manche, l'Ille et Vilaine et la Loire-Atlantique du Mont St Michel à Hoscas.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act4.png'
        },
        {
          name: 'La vallée du Couesnon',
          description: "Vener vous promener dans la vallée du couesnon",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act5.png'
        },
        {
          name: 'Activités sportives',
          description: "randonnée, VTT, escalade, canöe-kayak, accrobranche",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act15.png'
        },
       
        {
          name: 'Mont Saint Michel',
          description: "Profiter de votre séjour en bretagne pour faire votre traversée de la baie et visiter l'une des 7 merveilles du monde.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act9.png'
        },
        {
          name: 'Saint Malo',
          description: "La cité corsaire vous acceuil avec ses grandes plages de sables fin, ses restaurants étoilés. Intra-muros vous fera perdre la notion du temps.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act10.png'
        },
        {
          name: 'Cancale',
          description: "Que diriez-vous d'un magnifique plateau de fruits de mer ? Vous êtes à la bonne adresse.",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act11.png'
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