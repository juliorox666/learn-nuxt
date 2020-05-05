<template>
  <v-toolbar app class="header">
    <v-toolbar class="box-header white--text" justify-center flat>
      <v-toolbar-title class="titulo-home">
        <nuxt-link to="/">Blueticket</nuxt-link>
      </v-toolbar-title>
      <v-text-field
        flat
        solo
        hide-details
        prepend-inner-icon="search"
        label="Search"
        class="hidden-sm-and-down box-procura"
      ></v-text-field>
      <v-menu
        v-model="menu"
        :close-on-content-click="false"
        :nudge-width="200"
        offset-x>
        <v-btn class="white--text" flat slot="activator">
          Florianópolis
          <v-icon>keyboard_arrow_down</v-icon>
        </v-btn>

        <v-card>
          <v-list>

              <v-list-tile>
                <v-list-tile-content>
                  <v-list-tile-title>São Paulo</v-list-tile-title>
                </v-list-tile-content>

                <v-list-tile-action>
                  <v-icon>keyboard_arrow_down</v-icon>
                </v-list-tile-action>
              </v-list-tile>

              <v-list-tile>
                <v-list-tile-content>
                  <v-list-tile-title>Belo Horizonte</v-list-tile-title>
                </v-list-tile-content>

                <v-list-tile-action>
                  <v-icon>keyboard_arrow_down</v-icon>
                </v-list-tile-action>
              </v-list-tile>
          </v-list>
        </v-card>
      </v-menu>
      <v-spacer></v-spacer>
      <v-btn icon class="white--text">
        <v-icon>favorite_border</v-icon>
      </v-btn>
      <v-btn icon class="white--text">
        <v-icon>notifications</v-icon>
      </v-btn>
      <v-btn icon large>
        <v-avatar size="32px" tile>
          <img
            src="https://cdn.vuetifyjs.com/images/logos/logo.svg"
            alt="Vuetify"
          >
        </v-avatar>
      </v-btn>
    </v-toolbar>
  </v-toolbar>
</template>

<script>
export default {
  data () {
    return {
      menu: ''
    }
  }
}
</script>

<style>
.header {
  background-color: #1867c0 !important;
}
.box-header {
  width: 1215px;
  background-color: #1867c0 !important
}
.titulo-home {
  width: 200px;
}
.box-procura {
  width: 388px;
  max-width: 388px;
  background-color: #fff;
  border-radius: 100px;
}
.box-procura * {
  background: transparent !important;
}
</style>
