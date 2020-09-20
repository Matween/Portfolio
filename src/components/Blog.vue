<template>
<div class="blog-posts">
    <div class="blog-posts-row">
        <Preview class="blog-posts-col" :preview="this.blog" v-on:click="openLink(this.blog.url)" />
    </div>
</div>
</template>

<script>
import Preview from './Preview.vue'
export default {
    name: 'Blog',
    components: {
        Preview
    },
    data() {
        return {
            blog: {
                name: 'Blog',
                img: 'https://lukaszadam.com/assets/downloads/old-computer-illustration.png',
                description: 'Read my blog...',
                url: 'https://matween.wordpress.com/'
            }
        }
    },
    methods: {
        openLink(url) {
            window.open(url, "_blank");
        }
    }
}
</script>

<style>
@media (max-width: 1200px) {
    .blog-posts-col {
        width: 90% !important;
    }
}

.blog-posts {
    margin: 3em;
}

.title {
    width: 100% !important;
    margin: auto;
}

.blog-posts-row {
    width: 100%;
    margin: auto;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: -moz-flex;
    display: -webkit-flex;
    display: flex;
    -webkit-flex-flow: wrap row;
    flex-flow: wrap row;
    align-items: center;
    justify-content: center;
}

.blog-posts-col {
    width: 350px !important;
}

.blog-posts-col:hover {
    cursor: pointer;
}

h2 {
    text-align: center;
}
</style>
