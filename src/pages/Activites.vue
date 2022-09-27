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
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act1.png'
        },
        {
          name: 'Vieux Rennes',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act2.png'
        },
        {
          name: 'Rennes',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act3.png'
        },
        {
          name: 'Gr34',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act4.png'
        },
        {
          name: 'La vallée du Couesnon',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act5.png'
        },
        {
          name: "Base d'activité de la Méziere",
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act6.png'
        },
        {
          name: 'Canöe Kayak',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act7.png'
        },
        {
          name: 'Escalade',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act8.png'
        },
        {
          name: 'Accrobranche',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act12.png'
        },
        {
          name: 'Mont Saint Michel',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act9.png'
        },
        {
          name: 'Saint Malo',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
          image: 'https://raw.githubusercontent.com/Sanitc/ma-project/master/src/assets/img/act/act10.png'
        },
        {
          name: 'Cancal',
          description: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s,",
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