<template>
  <footer id="footer">
    <span class="copyright">&copy; 2022 {{ copyright }}.</span>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      copyright: '',
    }
  },
  methods:{
    async getFooterData(){
      const res = await fetch('https://api.p10i.it/api/home/footer')
      let json_res = await res.json()

      this.copyright = json_res.copyright
    }
  },
  mounted() {
    this.getFooterData()
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
