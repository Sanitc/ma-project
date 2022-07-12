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
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                  Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                  when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>

                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                  Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                  when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>

                  <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                  Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                  when an unknown printer took a galley of type and scrambled it to make a type specimen book. </p>

                  <v-btn color="brown"             
                   href="#reservation"
                  @click="$vuetify.goTo('#reservation')"          
                  >
                  <span class="reserve-btn">Réserver</span>
                  </v-btn>           
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
                      <v-img contain :src="item.src" aspect-ratio="1" class="img-grid">
                        <template v-slot:placeholder>
                          <v-row class="fill-height ma-0" align="center" justify="center">
                            <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                          </v-row>
                        </template>
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
  text-align: center;
  margin-top: 2%;
  margin-right:10% ;
  margin-left:10% ;
  
}
.gite-img{
  height: 100;
  width: 100;
}
.reserve-btn{
  color:white;
}
.img-grid{
  
  height: 284px;
  width: 400px;
  
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
      ]
    };
  }
};
</script>