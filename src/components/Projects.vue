<template>
<div class="projects">
    <div class="title">
        <h2>Projects</h2>
    </div>
    <div class="projects-row">
        <Preview class="projects-col" v-for="project in projects" v-bind:key="project" v-bind:preview="project" />
    </div>
</div>
</template>

<script>
import Preview from './Preview.vue'
export default {
    name: 'Projects',
    components: {
        Preview
    },
    data() {
        return {
            projects: [{
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                },
                {
                    name: 'Test',
                    description: 'Omg ftow. This looks awesome, or maybe not. Not sure. Lorem ipsum ftw.',
                    img: 'https://images.pexels.com/photos/303383/pexels-photo-303383.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260'
                }
            ]
        }
    },
}
</script>

<style>
@media (max-width: 1200px) {
    .projects-col {
        width: 90% !important;
    }
}

.projects {
    margin: 3em;
}

.title {
    width: 100% !important;
    margin: auto;
}

.projects-row {
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
