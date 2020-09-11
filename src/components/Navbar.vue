<template>
<nav>
    <div class="links">
        <router-link class="link" to="/">Home</router-link>
        <router-link class="link" to="/blog">Blog</router-link>
        <router-link class="link" to="/contact">Contact</router-link>
    </div>
</nav>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

<style>
nav {
    margin-left: auto;
    margin-right: auto;
    padding: 1.5em;
    height: 40px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.links {
    margin: auto;
}

.link {
    padding: 0 0.5em;
    text-transform: uppercase;
    text-decoration: none;
    color: #415268;
}

.link:hover {
    font-weight: bold;
}

.link:visited {
    color: #415268;
}
</style>
