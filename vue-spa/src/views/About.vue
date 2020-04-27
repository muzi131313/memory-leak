<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button id="btn" @click="back">back</button>
    <ul id="ul" ref="ul">
      <li v-for="(image, key) in images" :key="key">
        image: {{image.src}}
        <image :src="image.src" width="100px"></image>
      </li>
    </ul>
  </div>
</template>
<script>
const NUM = 10000

export default {
  name: 'About',
  data () {
    return {
      images: []
    }
  },
  created () {
    this.initData()
  },
  methods: {
    initData () {
      for (let i = 0; i < NUM; i++) {
        this.images.push({
          src: 'https://alipic.lanhuapp.com/webd6b1e153-7375-4843-9c46-c520a1c36127?x-oss-process=image/resize,h_234/format,webp'
        })
      }
    },
    back () {
      this.$router.back()
    }
  }
}
</script>
<style scoped>
#btn {
  margin: 30px 0;
}
#ul {
  height: 100px;
  overflow-y: scroll;
}
#ul li {
  width: 100%;
  height: 30px;
}
</style>
