<template>
  <v-app>
    <div>
      <h1 class="main-title">
        Hauptseite
      </h1>
      <v-btn 
        color="primary"
        nuxt
        to="/test"
      >
        Komponentenbibliothek
      </v-btn>
    </div>
  </v-app>
</template>

<script>

export default {
  name: 'IndexPage',
}
</script>

<style>
.main-title {
  padding: 50px 0 25px 0;
}
</style>