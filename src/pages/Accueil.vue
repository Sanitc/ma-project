<template>
  <section id="accueil" class="accueil-section">
    
    <v-container>
      
      <div class="center">        
          <h1 class="acceuil-title">Gîte de la Bergère</h1>
          <p></p>
          <div class="acceuil-text">
            <p>Meublé de tourisme X étoiles</p>
            <p>Labelisation gîte de France X épis</p>
            <p>Paiement accepté : ANCV Chèques vacances </p>
          </div>  
      </div>
      
    </v-container>
  </section>
</template>

<style scoped>
.accueil-section{
   background: url('../assets/img/accueil/accueil-background.jpg')
    no-repeat center center fixed;
  background-size: cover;
  height: 10%;
}
/*.accueil-section{
  background: #795548;
  
}*/
.center-about{
  padding-top: 5%;
  padding-left: 10%
}
.center{
  margin-top: 10%;
  margin-right: 10%;
  margin-left: 10%;
  text-align: left;
  font-size: 150%;
  color: white;
}
.acceuil-title{
 font-weight: 350;
 font-size: 4rem;
 color: white;
}
.acceuil-text{
  font-weight: 300;
  font-size: 1.5rem;
  color: white;
}


</style>
