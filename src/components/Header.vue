<template>
  <header id="header">
    <h1>{{ title }}</h1>
    <p>HS Student &nbsp;&bull;&nbsp; Self-taught WebDev &nbsp;&bull;&nbsp; Photographer</p>
    <nav>
      <ul>
        <li v-for="btn in btns" :key="Object.keys(btn)[0]">
          <a :href="Object.values(btn)[0][1]" :class="Object.values(btn)[0][0]" class= "icon" ><span class="label">{{ Object.keys(btn)[0] }}</span></a>
        </li>

      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      title: '',
      btns: []
    }
  },
  methods:{
    async getHeaderData(){
      const res = await fetch('https://api.p10i.it/api/home/title-page')
      let json_res = await res.json()

      this.title = json_res.title
      this.btns = json_res.btns
    }
  },
  mounted() {
    this.getHeaderData()
  },
}
</script>