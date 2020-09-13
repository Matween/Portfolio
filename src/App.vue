<template>
<div class="content">
    <Sidebar />
    <Content />
</div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import Content from './components/Content.vue'
export default {
    name: 'App',
    components: {
        Sidebar,
        Content
    }
}
</script>

<style lang="scss">
.content {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

html,
body {
    background-image: url('https://images.pexels.com/photos/266451/pexels-photo-266451.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    overflow-x: hidden;
}
</style>
