<template>
    <article>
        <nuxt-content :document="article" />
    </article>
</template>

<script>
export default {
    async asyncData({ $content, params }) {
        const article = await $content('blog', params.slug).fetch();

        return { article }
    }
}
</script>

<style>
    article {
        display: block;
        margin: 0 auto;
        padding: 50px 30px;
        max-width: 800px;
    }
    h1 {
        font-size: 30px;
        font-weight: 700;
        margin-bottom: 30px;
        color: #191F28;
    }
    p {
        font-weight: 300;
        font-size: 18px;
        text-decoration: none;
        color: #454F5D;
    }
</style>