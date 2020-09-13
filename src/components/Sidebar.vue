<template>
<aside>
    <Navbar />
    <ImageTile image="https://static.fandomspot.com/images/06/7234/00-featured-izuku-midoriya-boku-no-hero-academia-anime-screenshot.jpg" fullName="Matic Bozic" />
    <div class="description">
        <div class="about">
            Hi, I am a full-stack developer with a wide range of skills, <br>
            If I'm not developing web sites, I am dabbling in Linux and Unix systems.
        </div>
        <h3 class="skills-title">SKILLS</h3>
        <div class="skills">
            <div class="skill" v-for="skill in skills" v-bind:key="skill">{{ skill }}</div>
        </div>
    </div>
    <div class="social">
        <a :href="github">
            <img src="https://upload-icon.s3.us-east-2.amazonaws.com/uploads/icons/png/13855371531555590081-512.png" alt="">
        </a>
    </div>
</aside>
</template>

<script>
import ImageTile from './ImageTile.vue';
import Navbar from './Navbar.vue';
export default {
    name: 'Sidebar',
    components: {
        Navbar,
        ImageTile,
    },
    data() {
        return {
            skills: [
                "HTML",
                "CSS",
                "Javascript",
                "Python",
                "PHP",
                "Vue",
                "Flask",
                "Angular.js",
                "Laravel",
                "Docker",
                "Vagrant",
                "Heroku",
                "Linux",
                "SQL"
            ],
            github: "https://github.com/Matween"
        }
    }
}
</script>

<style lang="scss">
@media (max-width: 1200px) {
    aside {
        min-width: 100vw !important;
        float: left !important;
        position: absolute !important;
        display: flex !important;
        flex-direction: column !important;
    }

    aside>div {
        flex: 1 !important;
    }
}

aside {
    background-color: #c4d6ebc2;
    position: fixed;
    height: 100%;
    width: 30%;
    top: 0;
    bottom: 0;
    left: 0;
}

.description {
    color: #415268;
}

.social {
    width: 60%;
    margin: auto;
    display: flex;
    justify-content: center;
}

.social img {
    padding-top: 2em;
    width: 40px;
    height: 40px;
    transition: transform .2s;
}

.social img:hover {
    transform: scale(1.05);
}

.about {
    text-align: center;
    padding: 1em;
}

.skills-title {
    text-align: center;
}

.skills {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 65%;
    margin: auto;
}

.skill {
    margin: 0.5em;
    color: #eef9ff;
    font-weight: bold;
    background-color: #607999;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 1em;
    padding: 0.5em;
    -webkit-touch-callout: none;
    /* iOS Safari */
    -webkit-user-select: none;
    /* Safari */
    -khtml-user-select: none;
    /* Konqueror HTML */
    -moz-user-select: none;
    /* Old versions of Firefox */
    -ms-user-select: none;
    /* Internet Explorer/Edge */
    user-select: none;
    transition: transform .2s;
}

.skill:hover {
    transform: scale(1.05);
}
</style>
