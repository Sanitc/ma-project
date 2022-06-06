<template>
    <section  id="header" class="header-section">
        <v-app>
            
            <v-navigation-drawer width="240px" permanent fixed> 
            <div class="menu">
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
                    
                    <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
                </v-list>
            </div>  
            </v-navigation-drawer>
            <v-main>
            <slot/>
            </v-main>
        </v-app>
    </section>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: 'Accueil'},
        { title: 'Le Gite'},
        { title: 'Prestations'},
        { title: 'Réservation'},
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