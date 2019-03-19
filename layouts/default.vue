<template>
<v-app>
  <Nav/>
  <nuxt/>
  <Footer/>
</v-app>

</template>

<script>
import Nav from "./UI/nav";
import Footer from './UI/footer';
export default {
  components: {
    Nav,
    Footer
  },
};
</script>
