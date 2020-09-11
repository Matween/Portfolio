<template>
<div class="content">
    <Sidebar />
    <Content />
</div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import Content from './components/Content'
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

body {
    background: url('https://images.pexels.com/photos/266451/pexels-photo-266451.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
    overflow-x: hidden;
}

$particleSize: 20vmin;
$animationDuration: 6s;
$amount: 20;

body .particle {
    width: $particleSize;
    height: $particleSize;
    border-radius: $particleSize;
    backface-visibility: hidden;
    position: absolute;
    animation-name: move;
    animation-duration: $animationDuration;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    $colors: (#c4d6eb,
            #607999,
            #609991);

    @for $i from 1 through $amount {
        &:nth-child(#{$i}) {
            color: nth($colors, random(length($colors)));
            top: random(100) * 1%;
            left: random(100) * 1%;
            animation-duration: (random($animationDuration * 10) / 10) * 1s + 10s;
            animation-delay: random(($animationDuration + 10s) * 10) / 10 * -1s;
            transform-origin: (random(50) - 25) * 1vw (random(50) - 25) * 1vh;
            $blurRadius: (random() + 0.5) * $particleSize * 0.5;
            $x: if(random() > 0.5, -1, 1);
            box-shadow: ($particleSize * 2 * $x) 0 $blurRadius currentColor;
        }
    }
}

@keyframes move {
    100% {
        transform: translate3d(0, 0, 1px) rotate(360deg);
    }
}
</style>
