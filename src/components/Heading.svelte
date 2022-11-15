<script lang="ts">
    import { fly, scale } from 'svelte/transition';
    import { OnMount } from 'fractils';

    let innerHeight = 0;
    let innerWidth = 0;
    let timer = 1500;
</script>

<svelte:window bind:innerHeight bind:innerWidth />

<OnMount>
    <div
        class="heading"
        in:scale={{
            duration: timer,
            start: innerWidth < 500 ? 1.3 : 2,
            opacity: 1,
            delay: timer,
        }}
    >
        <img
            class="heading-img"
            alt="Heading"
            aria-label="Heading"
            src="images/The_Woodys_Logo.png"
            in:fly={{
                duration: timer,
                y: innerHeight / 8,
                opacity: 1,
                delay: timer,
            }}
        />
    </div>
</OnMount>

<style>
    .heading-img {
        margin: 0 auto;
        display: block;
        box-shadow: none;
        transition: all 0.25s ease;
        overflow: hidden;
        align-self: center;
        max-height: 10vh;
    }

    .heading {
        position: relative;
        text-align: center;
        pointer-events: all;
        width: 100%;
        z-index: 11;
        margin-top: 1em;
        display: flex;
    }
</style>
