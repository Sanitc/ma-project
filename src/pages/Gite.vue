<template>
  <section id="gite" class="gite-section">
    
    <v-container>
      <div class="center-gite">
        <v-row>
          <v-col sm="6">
          <v-img
          
            :src="require('../assets/img/gite/gite.png')"
            class="gite-img"
          />
          </v-col>
          <v-col sm="6" class="d-flex flex-column justify-center ">
            <div>
              <h2 class="gite-title">Gite de la bergère</h2>
              <div class="gite-text">
                <div>
                  <p>Pour un week-end ou une semaine, profitez d’un gîte d’exception clé en main pouvant accueillir jusqu’à 9 personnes au sein d'un petit village.</p>

                  <p>Situé au bord de la vallée du Couesnon et de son domaine départemental, cette longère a été rénovée en gite tout confort, 
                    plein de charme. Un accès direct au Gr39 vous permettra de profiter pleinement de nombreuse activitées nature sur un terrain valonné.
                  Au terme de vos journées sportive, détendez-vous au calme en profitant du jacuzzi installé en plein air ou en passant d'agréable moment avec tout ce qui est mis à votre disposition.</p>

                  <p>Durant les périodes de vacances scolaires,
                    les séjours sont toujours du samedi au samedi suivant, les week ends sont du vendredi au dimanche.</p>
                </div>
                <div class="btn-reservation">
                    <v-btn color="brown"          
                    href="#reservation"
                  @click="$vuetify.goTo('#reservation')"          
                  >
                  <span class="reserve-btn">Réserver</span>
                  </v-btn> 
                </div>                          
              </div>              
            </div>   
          </v-col>
        </v-row>
      </div>
      <div class="grid-section">
        <v-row>
          <v-col sm="12" class="d-flex flex-column justify-center ">
            <div>
              <h2 class="gite-title">Un gite tout confort</h2>
              <div class="gite-grid">
                <v-row>
                  <v-col v-for="item in items" :key="item.id" class="d-flex child-flex" cols="6" sm="4">
                  
                    <v-card flat tile class="d-flex">
                      <v-img contain :src="item.src" aspect-ratio="1" class="img-grid" @click.stop="dialog = true">
                      </v-img>
                    </v-card>
                  </v-col>
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

.img{
  border-radius: 15px;
  box-shadow: 10px 5px 5px #ADAFBC
}
.center-gite{
  padding-top: 5%;
  padding-left: 10%;
  margin-bottom: 2%;
}
.center{
  padding-top: 5%;
  text-align: center;
  font-size: 150%;
}
.gite-title{
  text-align: center;
}
.gite-text{
  text-align: left;
  margin-top: 2%;
  margin-right:10% ;
  margin-left:10% ;
  
}
.btn-reservation{
  text-align: center;
}
.gite-img{
  margin-top: 15%;
  height: 100;
  width: auto;
  
  
}
.reserve-btn{
  color:white;
}
.img-grid{
  
  height: 284px;
  width: 400px;
}

.test{
  max-height: 100;
  width: 100;
}

.grid-section{
  margin-bottom: 2%;
}
.gite-grid{
  margin-top: 2%;
}
</style>

<script>



export default {
  name: "Gallery",
  data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/img/galerie/galerie1.png")
        },
        {
          id: 2,
          src: require("../assets/img/galerie/galerie2.png")
        },
        {
          id: 3,
          src: require("../assets/img/galerie/galerie3.png")
        },
        {
          id: 4,
          src: require("../assets/img/galerie/galerie4.png")
        },
        {
          id: 5,
          src: require("../assets/img/galerie/galerie5.png")
        },
        {
          id: 6,
          src: require("../assets/img/galerie/galerie6.png")
        },
        {
          id: 7,
          src: require("../assets/img/galerie/galerie7.png")
        },
        {
          id: 8,
          src: require("../assets/img/galerie/galerie8.png")
        },
        {
          id: 9,
          src: require("../assets/img/galerie/galerie9.png")
        }
      ],
      dialog: false,
      
    };
    
  },
};
</script>