<template>
  <v-toolbar color="#40e0d0">
    <v-toolbar-title class="white--text">Nuxtvify Jobs</v-toolbar-title>
    <v-toolbar-items class="white--text" router exact>
      <v-btn flat>
        <nuxt-link to="/">Home</nuxt-link>
      </v-btn>
      <v-btn flat>
        <nuxt-link to="/user">Users</nuxt-link>
      </v-btn>
    </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {};
</script>

<style >
a:visited,
a:link {
  color: white;
}
a {
  text-decoration: none;
}
</style>
