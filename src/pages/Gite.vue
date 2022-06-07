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
                  
                  <v-col
                    v-for="n in 9"
                    :key="n"
                    class="d-flex child-flex"
                    cols="4"
                          >
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="img-grid"
                    >       
                    </v-img>
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
.gite-section{

}
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

