<template>
  <article>
    <!--{{article}}-->
    <div>
      <img :src="require(`~/assets/resources/${article.img}`)" alt="">
    </div>
    <nuxt-content :document="article"/>
  </article>
</template>

<script>
export default {

  async asyncData({$content, params}){
    const article = await $content('blog', params.slug).fetch();
    return {article}
  }
}
</script>

<style scoped>
img {
  display: block;
  width: 100%;
  max-width: 500px;
  margin: auto;
}

article {
  display: block;
  margin: 0 auto;
  padding: 50px 30px;
  max-width: 800px;
}
h1 {
  font-size: 28px;
  font-weight: 900;
  margin-bottom: 30px;
}
</style>
