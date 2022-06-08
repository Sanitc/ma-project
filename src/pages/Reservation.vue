<template>
  <section id="reservation" class="reservation-section">
   <v-container>
      <div>
        <v-row>  
          <v-form class="contact-form"
                ref="form"
                v-model="valid"
                lazy-validation
               
            >
            <h1 class="form-title">Contacter-nous</h1>
                <v-text-field
                v-model="name"
                :counter="30"
                :rules="nameRules"
                label="Nom Prénom"
                required
                ></v-text-field>

                <v-text-field
                v-model="email"
                :rules="emailRules"
                label="E-mail"
                required
                ></v-text-field>

                <v-textarea
                v-model="message"
                :rules="messageRules"
                label="Message"
                required
                ></v-textarea>

                <v-btn
                :disabled="!valid"
                color="success"
                class="mr-4"
                @click="validate"
                >
                Envoyer
                </v-btn>

                <v-btn
                color="error"
                class="mr-4"
                @click="reset"
                >
                Effacer
                </v-btn>
            </v-form>        
        
           
        </v-row>
      </div>      
    </v-container> 
  </section>
</template>

<style scoped>
.reservation-section{
   background: url('../assets/img/accueil/accueil-background.jpg')
    no-repeat center center fixed;
  background-size: cover;
  height: 20%;
}

.contact-form{
    background-color: white;
    border-radius: 10px;
    width: 25%;
    padding-top: 2%;
    padding-bottom: 2%;
    padding-left: 2%;
    padding-right: 2%;
    margin-top: 2%;
    display: block;
    margin-left: auto;
    margin-right: auto ;
}

.form-title{
    color: saddlebrown;
}


</style>

<script>
  export default {
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'un nom est requis',
        v => (v && v.length <= 30) || 'Merci de mettre maximum 30 caratères',
      ],
      email: '',
      emailRules: [
        v => !!v || 'une adresse mail est requise',
        v => /.+@.+\..+/.test(v) || "L'e-mail n'est pas valide",
      ],
      message: '',
      messageRules: [
        v => !!v || 'un message est requis',
        v => (v && v.length >= 10) || 'Veuillez saisir un message de minimum 10 caractères',
      ],  
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      }
    },
  }
</script>