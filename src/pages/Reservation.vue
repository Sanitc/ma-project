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
                @click.stop="dialog = true"
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
        <v-dialog
      v-model="dialog"
      max-width="290"
    >
      <v-card>
        <v-card-title class="text-h5">
         Confirmation.
        </v-card-title>

          <v-card-text>
          Votre mail a bien été envoyer.
        </v-card-text>
     
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="red darken-1"
            text
            @click="dialog = false"
          >
            Retour
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
           
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
    height: 50%;
    width: auto;
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
      dialog: false,
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
        this.$refs.form.validate();
        this.$refs.form.reset();
      }
      },
      reset () {
        this.$refs.form.reset();
      }
      
  }
</script>