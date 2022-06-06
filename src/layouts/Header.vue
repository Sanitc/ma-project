<template>
  <v-app>
    <v-navigation-drawer width="240px" permanent fixed> 
      <div class="menu">
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title">
            Clément Le Saint
            </v-list-item-title>
            <v-list-item-subtitle>
              Développeur Junior
            </v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>
        
        <v-list
          dense
          nav
        >
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
            :to="`#${item.title.toLowerCase().replace(' & ', '-')}`"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </div>  
      <div class="contact">
        <h4 class="align">Contact</h4>
          <div class="align">   
              lesaint.c.dev@gmail.com
          </div>  
          <div>
          <a href="https://github.com/Sanitc" target="_blank">
                <img
                  class="contact-icon"
                  src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg"
                  
                >
          </a>
          <a href="https://www.linkedin.com/in/cl%C3%A9ment-le-saint-1a8083154/" target="_blank">
                <img
                  class="contact-icon"
                  src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg"
                >
              </a>
          </div> 
      </div>  
    </v-navigation-drawer>
    <v-main>
      <slot/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'A-propos', icon: 'mdi-account-box-outline' },
        { title: 'Projets', icon: 'mdi-apps' },
        { title: 'Compétences', icon: 'mdi-laptop' },
        { title: 'Educations & Expériences', icon: 'mdi-school-outline' },
        //{ title: 'Contact', icon: 'mdi-message-text-outline' },
      ]
    }
  }
}
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
html {
  scroll-behavior: smooth;
}

.v-application--wrap {

  flex-direction: row;
}

.contact {
  color: black;
  border-top: solid;
  border-width: 1px;
  border-color: #d8d8d8;
  text-align: center;
  padding-bottom: 5%;
}
.contact-icon {
  height: 30px;
  padding-left: 5%;
}

.v-main {
  flex: 1 0;
  margin-left: 240px;
}

.align {
  padding-bottom: 4%;
  padding-top: 2%;
  
}

.v-navigation-drawer__content{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}


</style>