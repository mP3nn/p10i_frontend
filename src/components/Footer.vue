<template>
  <footer id="footer">
    <span class="copyright">&copy; 2022 {{ copyright }}.</span>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    copyright : String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
