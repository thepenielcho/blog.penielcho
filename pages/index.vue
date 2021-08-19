<template>
  <div class="home-page">
    <!-- <Featured />
    <Banner1 /> -->
    <!-- <h2>Latest Posts</h2> -->
    <div class="articles">
        <div class="article" v-for="article of articles" :key="article">
          <nuxt-link class="article-nuxtlink" :to="{ name: 'slug', params: { slug: article.slug } }">
              <div class="article-inner">
                <img :src="require(`~/assets/resources/${article.img}`)" alt="" class="article-image"/>
                <!-- <img :src="require(`~/assets/resources/${article.img}`)" alt="" class="article-hover-image" /> -->
                <div class="detail">
                    <p class="category">{{article.category}}</p>
                    <h3 class="title">{{ article.title }}</h3>
                    <p class="datetime">{{ article.datetime }}</p>
                </div>
              </div>
          </nuxt-link>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content('blog', params.slug)
      .only(['title', 'description', 'img', 'datetime', 'category', 'author', 'slug'])
      // .sortBy('createdAt', 'asc')
      .sortBy('datetime', 'desc')
      .fetch();
    return {
      articles
    }
  }
}
</script>

<style scoped>
  .home-page {
    padding: 2.8rem 1.8rem;
  }
  .articles {
    margin: 0 auto;
    max-width: 1080px;
    /* background-color: lightslategrey; */
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .article{
    margin: 1rem 0 2rem;
    display: inline-flex;
    width: 50%;
    /* height: ; */
    /* display: flex; */
    /* justify-content: space-between; */
  }
  .article:hover .article-nuxtlink .detail .title{
    color: #3182F6;
    transition: 0.2s;
  }
  .article:hover .article-nuxtlink .article-inner .article-image{
    box-shadow: 0 0.2rem 2rem 0.8rem rgba(0,0,0,.13);
    /* offset-x | offset-y | blur-radius | spread-radius | color */
    position: relative;
    transform: translate(0, -0.2rem);
    transition: 0.3s;
  }
  .article-inner{
    margin: 0 auto;
    position: relative;
    max-width: 90%;
  }
  .article-inner img {
    width: 100%;
    max-width: 100%;
    /* max-height: 19rem; */
    border-radius: 1rem;
    box-sizing: border-box;
    margin-bottom: 0.7rem;
  }
  .article-inner .detail{
    padding: 1rem 0rem;
  }
  .category{
    color: #8B95A1;
    font-weight: 400;
    font-size: 0.85rem;
    padding-bottom: 0.8rem;
  }
  .title{
    color: #333D4B;
    font-weight: 600;
    font-size: 1.8rem;
    padding-bottom: 0.8rem;
  }
  .datetime{
    color: #8B95A1;
    font-weight: 400;
    font-size: 0.85rem;
  }
  /* h2 {
    margin-bottom: 30px;
    text-align: center;
  }
  .articles {
    margin: 0 auto
  components: { articles },;
    max-width: 800px;
  }
  .article {
    margin
  components: { articles },-bottom: 15px;
  }
  .article-inner {
    padding: 15px;
    background: #FFF;
    box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    display: flex;
  }
  .article-inner img {
    display: block;
    width: 100%;
    max-width: 300px;
  }
  .article-inner .detail {
    padding-left: 15px;
    padding-right: 15px;
  }
  h3 {
    color: #212121;
    font-size: 24px;
    text-decoration: none;
  }
  p {
    color: #888;
    font-size: 18px;
    text-decoration: none;
  } */
</style>
