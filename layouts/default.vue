<template>
<v-app dark>
    <v-app-bar :clipped-left="clipped" fixed app color="#8B0000">
        <v-toolbar-side-icon>
        <v-img src="../assets/sign/logomfu.png" />
        </v-toolbar-side-icon>  
        <v-toolbar-title class="white--text" v-text="title.title" />
        <v-spacer />
        <v-row class="v-text-field">
            
        </v-row>
        <v-spacer />
         
    </v-app-bar>
    <v-main>
        <v-container>
            <Nuxt />
        </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app height="100" color="#000000">
        <v-toolbar-title class="white--text" v-text="title.title" />
        <div></div>
        <v-spacer />
        <v-toolbar-title class="mx-4 white--text" v-text="title.about" />
        <v-divider class="mx-4" inset vertical></v-divider>

        <v-spacer />
         <v-btn
            class="mx-2"
            fab
            dark
            small
            color="primary"
            >
        <v-icon dark>
            mdi-facebook
        </v-icon>
        </v-btn>

        <v-btn
            class="mx-2"
            fab
            dark
            small
            color="primary"
            >
        <v-icon dark>
            mdi-youtube
        </v-icon>
        </v-btn>

        <v-btn
            class="mx-2"
            fab
            dark
            small
            color="primary"
            >
        <v-icon dark>
            mdi-folder
        </v-icon>
        </v-btn>
    </v-footer>
</v-app>
</template>

<script>
export default {
    name: 'DefaultLayout',
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: {
                title: 'Mae Fah Luang University',
                about: 'Contact Us : Registrar Division, Mae Fah Luang UniversityAS Building, 1st floor, Room 107 and 108'
               
            }
        }
    }
}
</script>

<style scoped>
.v-text-field {
      color: #3F3252;
   
  }
</style>