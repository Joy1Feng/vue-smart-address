<template>
  <div class="about">
    <h1>This is an about page</h1>
    <textarea @change="smart" cols="50" rows="10" v-model="info" placeholder="请粘贴你的地址"></textarea>
    <div v-html="parseInfo"></div>
  </div>
</template>
<script>
export default {
  name: 'About',
  components: {
  },
  data () {
    return {
      info: '',
      parseInfo: ''
    }
  },
  methods: {
    smart () {
      let parseList = parse(this.info)
      let html = ''
      for (let key in parseList) {
        if (parseList[key]) {
          html += `<p>` + key + `:` + parseList[key] + `</p>`
        }
      }
      this.parseInfo = html
    }
  },
  mounted () {
    parseArea(areaList)
  }
}
</script>
