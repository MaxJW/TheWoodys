<script lang="ts">
</script>

<div id="blur" />

<style>
    #blur {
        top: 0;
        left: 0;
        z-index: 99;
        width: 100vw;
        height: 100vh;
        position: fixed;
        pointer-events: none;
        animation-delay: 1.5s;
        animation-direction: normal;
        animation-duration: 1.5s;
        animation-fill-mode: forwards;
        animation-iteration-count: 1;
        animation-name: blur;
        backdrop-filter: blur(4px);
        -webkit-backdrop-filter: blur(4px);
        background-color: rgba(0, 0, 0, 0.7);
    }

    @keyframes blur {
        from {
            backdrop-filter: blur(4px);
            -webkit-backdrop-filter: blur(4px);
            background-color: rgba(0, 0, 0, 0.7);
        }

        to {
            backdrop-filter: blur(0px);
            -webkit-backdrop-filter: blur(0px);
            background-color: rgba(0, 0, 0, 0);
        }
    }
</style>
