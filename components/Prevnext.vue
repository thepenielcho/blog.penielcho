<template>
    <div class="prevnext-container">
        <div class="prev-container">
            <div class="prev-nav">Previous Post</div>
            <NuxtLink class="prev-link" v-if="prev" :to="{ name: 'slug', params: { slug: prev.slug } }">
            {{ prev.title }}
            </NuxtLink>
            <span v-else>이전 포스트가 없습니다.</span>
        </div>
        <div class="next-container">
            <div class="next-nav">Next Post</div>
            <NuxtLink class="next-link" v-if="next" :to="{ name: 'slug', params: { slug: next.slug } }">
            {{ next.title }}
            </NuxtLink>
            <span v-else>다음 포스트가 없습니다.</span>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
        prev: {
            type: Object,
            default: () => null
        },
        next: {
            type: Object,
            default: () => null
        }
        }
    }
</script>

<style scoped>
.clearfix::after{
    content: "";
    clear: both;
    display: block;
}
.prevnext-container{
    display: flex;
    justify-content: space-between;
    margin: 4rem auto;
    /* background-color: lightsteelblue; */
    max-width: 800px;
}
.prev-container{
    padding: 2.3rem 3rem;
    width: 45%;
    background-color: #F2F4F6;
    
    border-radius: 1rem;
}
.prev-container .prev-nav{
    color: #444F61;
    font-weight: 600;
    font-size: 1.35rem;
    margin: 0 0 1rem;
}
.prev-container .prev-link{
    color: #333D4B;
    font-weight: 400;
    font-size: 1.1rem;
    word-break: keep-all;
    line-height: 1.3;
    display: block;
}
.next-container{
    padding: 2rem 4rem;
    width: 45%;
    background-color: #F2F4F6;
    border-radius: 1rem;
}
.next-container .next-nav{
    color: #444F61;
    font-weight: 600;
    font-size: 1.35rem;
    margin: 0 0 1rem;
    float: right;
    text-align: right;
    width: 100%;
}
.next-container .next-link{
    color: #333D4B;
    float: right;
    font-weight: 400;
    font-size: 1.1rem;
    text-align: right;
    word-break: keep-all;
    line-height: 1.3;
}
.next-container span{
    float: right;
    text-align: right;
}
</style>

#2178FF;
#323D4B;
F2F4F6

#F5F5F5
F8FAFC

.prev-container{
    padding: 2.3rem 3rem;
    width: 45%;
    background-color: #E9F2FF;
    
    border-radius: 1rem;
}
.prev-container .prev-nav{
    color: #1B64DA;
    font-weight: 600;
    font-size: 1.35rem;
    margin: 0 0 1rem;

이 조합은 hover로 사용하도록 하자~