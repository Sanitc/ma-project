<template>
  <section id="reservation" class="reservation-section">
    
    <v-container>
      <div class="center-gite">
        <v-row>
          <v-col sm="6">
            <div>
              <h1 class="contact-title">Contactez-nous</h1>
              <p></p><p></p>
              <div class="contact-text">                 
                  <p><span><v-icon color="white">mdi-email</v-icon>  gitedelabergere@gmail.com</span></p>
                  <p><span><v-icon color="white">mdi-phone</v-icon>  00 11 22 33 44</span></p>
                  <p><span><v-icon color="white">mdi-map-marker</v-icon>  La bergère, 35140 Mézières-sur-Couesnon</span></p>                    
              </div>                
            </div> 
          </v-col>
          <v-col sm="6" class="d-flex flex-column justify-center ">
            <div>
              <v-row>  
                <div class="container">
                  <form id="form" class="contact-form" ref="form" @submit.prevent="sendEmail">
                    <h1 class="form-title">Formulaire de contact</h1>
                    <input type="text" name="name" placeholder="Nom Prénom" required>
                    <p></p>
                    <input type="email" name="email" placeholder="E-mail" required>
                    <p></p>
                    <textarea name="message" placeholder="Message" required></textarea>
                    <p></p>
                    <button type="submit" value="Submit">ENVOYER</button>
                  </form>
                </div>               
              </v-row>
             </div> 
          </v-col>
        </v-row>
      </div>
    </v-container>
  </section>
</template>

<style scoped>
/*.reservation-section{
  background: #795548;
}*/


.reservation-section{
   background: url('../assets/img/accueil/accueil-background.jpg')
    no-repeat center center fixed;
  background-size: cover;
  height: 13%;
}

.center-gite{
  padding-top: 5%;
  padding-left: 10%;
}

.contact-title{
 font-weight: 300;
 font-size: 4rem;
 color: white;
}

.contact-text{
  font-weight: 300;
  font-size: 1.5rem;
  color: white;
}

.contact-form{
  background-color: white;
  border-radius: 10px;
  
    padding-top: 2%;
    padding-bottom: 2%;
    padding-left: 2%;
    padding-right: 2%;
    margin-top: 2%;
    display: block;
    margin-left: auto;
    margin-right: auto ;
}

* {box-sizing: border-box;}


label {
  float: left;
}

input[type=text], [type=email], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  margin-top: 6px;
  margin-bottom: 16px;
  resize: vertical;
}

button[type=submit] {
  background-color: #4CAF50;
  color: white;
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #45a049;
}

</style>
<script>
 import emailjs from 'emailjs-com';
    //Send mail
    export default {
            methods: {
        sendEmail() {
          emailjs.sendForm('service_voh8gcf', 'template_ttsxwhn', this.$refs.form, 'd-Qv09SkEavmBppQp')
            .then((result) => {
                console.log('SUCCESS!', result.text);
                
                
            }, (error) => {
                console.log('FAILED...', error.text);
            });
        }
      }
    }

//Clear form
document.addEventListener("submit", function(event) {
event.preventDefault() 
event.target.reset()
window.alert(" Votre mail a bien été envoyer!")
})


</script>
