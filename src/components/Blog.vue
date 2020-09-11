<template>
<div class="blog-posts">
    <div class="title">
        <h2>Blog</h2>
    </div>
    <div class="blog-posts-row">
        <Preview class="blog-posts-col" v-for="(post, index) in posts" v-bind:key="index" :preview="post" />
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
            posts: [{
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Blog Post',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/1793525/pexels-photo-1793525.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                }
            ]
        }
    }
}
</script>

<style>
@media (max-width: 1200px) {
    .blog-posts-col {
        width: 100% !important;
    }
}

.blog-posts {
    margin: 2em;
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

h2 {
    text-align: center;
}
</style>
