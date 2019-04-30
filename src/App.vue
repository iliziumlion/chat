<template>
  <v-app>
	<!-- Toolbar   -->
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span class="font-weight-light">Chat</span>
      </v-toolbar-title>
	  <v-flex xs11>
        <v-img
          :src="require('./assets/logo.svg')"
          class="my-3"
          contain
          height="50"
        ></v-img>
		</v-flex>
      <v-spacer></v-spacer>
    </v-toolbar>
	<!-- Content   -->
    <v-content>
      <Chat/>
    </v-content>
	<v-footer
	    height="auto"
	    color="primary lighten-1"
	  >
	    <v-layout
	      justify-center
	      row
	      wrap
	    >
	      <v-flex
	        primary
	        lighten-2
	        py-3
	        text-xs-center
	        white--text
	        xs12
	      >
	        &copy;2018 — <strong>Vuetify</strong>
	      </v-flex>
	    </v-layout>
	  </v-footer>
  </v-app>
</template>

<script>
import Chat from './components/Chat'

export default {
  name: 'App',
  components: {
    Chat
  },
  data () {
    return {

    }
  }
}
</script>
