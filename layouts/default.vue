<template>
  <div>

    <v-card class="overflow-hidden"></v-card>

    <v-toolbar
      height="100px"
      dark
      prominent
    >
      <v-toolbar-title> Dongeto</v-toolbar-title>


      <v-spacer></v-spacer>

      <v-btn
        v-if="$route.params.slug != undefined"
        @click="logout()"
        class="mr-2 mt-5 "
        color=#F50057
        small
        fab
      >
        <v-icon>mdi-logout</v-icon>
      </v-btn>
      <NuxtLink :to="{ path: '/account/' + this.slug}">
        <v-btn
          v-if="$route.params.slug != undefined"
          class="mr-2 mt-5 "
          color=#545237
          small
          fab
        >
          <v-icon>mdi-account-circle</v-icon>
        </v-btn>
      </NuxtLink>
    </v-toolbar>
    <v-app>

      <v-parallax
        dark
        src="https://wallpapercave.com/wp/wp9346055.jpg"

        height="auto"
      >
        <nuxt/>

      </v-parallax>
    </v-app>
    <v-footer
      dark
      padless
    >
      <v-card
        class="flex"
        flat
        tile
      >
        <v-card-title class="purple">
          <strong class="subheading">Get connected with Designer & devoloper on social networks!</strong>
          <v-spacer></v-spacer>
          <v-btn
            target="_blank"
            href="https://www.instagram.com/devoloper_soroosh/"
            class="mx-4"
            icon
          >
            <v-icon size="24px">
              mdi-instagram
            </v-icon>
          </v-btn>
          <v-btn
            target="_blank"
            href="https://api.whatsapp.com/send/?phone=989035894088&text&app_absent=0"
            color="green white--text"
            class="mx-4"
            icon
          >
            <v-icon size="24px">
              mdi-whatsapp
            </v-icon>
          </v-btn>
          <v-btn
            target="_blank"
            href="https://gitlab.com/sorooshmorshedi"
            color="green white--text"
            class="mx-4"
            icon
          >
            <v-icon size="24px">
              mdi-gitlab
            </v-icon>
          </v-btn>

          <v-btn
            target="_blank"
            href="https://github.com/Sorooshmorshedi"
            color="green white--text"
            class="mx-4"
            icon
          >
            <v-icon size="24px">
              mdi-github
            </v-icon>
          </v-btn>


          <v-btn
            target="_blank"
            href="https://www.linkedin.com/in/sorooshmorshedi/"
            class="mx-4"
            icon
          >
            <v-icon>
              mdi-linkedin
            </v-icon>
          </v-btn>

        </v-card-title>

        <v-card-text class="py-2 deep-purple text-center">
          {{ new Date().getFullYear() }}/{{ new Date().getMonth() }}/{{ new Date().getUTCDate() }} — <strong>Soroosh
          morshedi</strong>
        </v-card-text>
      </v-card>
    </v-footer>


  </div>


</template>

<script>

export default {
  name: 'DefaultLayout',
  data() {
    return {
      slug: this.$route.params.slug,
      myid: this.$route.query.acid,

    }
  },
  methods: {
    logout() {
      window.location.href = 'http://127.0.0.1:8000/logout'
    }
  }
}
</script>
<style>
body {
  background-color: #333399;
}

h.mytitle {
  color: #66cccc;
  padding-left: 30px;
  padding-bottom: 30px;
  size: 100px;
  text-shadow: 2px 2px 2px #333399;
  font-size: xxx-large;


}
</style>
