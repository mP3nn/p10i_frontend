<template>
    <div id="main">
      <Header></Header>
      <Footer copyright="Marco Pennacchioni"></Footer>
    </div>
</template>

<script>
import Header from "@/components/Header";
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
  },
}
</script>

