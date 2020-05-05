<template>
  <v-app>
    <app-header />
    <v-content>
      <v-container fluid grid-list-xl class="content">
        <nuxt />
      </v-container>
    </v-content>
    <v-footer app></v-footer>
  </v-app>
</template>

<script>
import AppHeader from '@/components/header'

export default {
  components: {
    AppHeader
  }
}
</script>

<style>
.content {
  width: 1215px;
}
</style>
