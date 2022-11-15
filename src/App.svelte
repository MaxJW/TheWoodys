<script lang="ts">
    import { onMount } from 'svelte';
    import Blur from './components/Blur.svelte';
    import Content from './components/Content.svelte';
    import CustomParticles from './components/CustomParticles.svelte';
    import Heading from './components/Heading.svelte';

    /* Force window back to top on reload */
    onMount(async () => {
        window.addEventListener('unload', function (e) {
            window.scrollTo(0, 0);
        });
    });
</script>

<Heading />
<!-- Anything above will never be blurred -->

<Blur />

<p style="text-align: center; color: #beba9f;">Sponsored by Young Sheldon</p>
<div class="desc">
    <div class="image">
        <img src="images/presenter.png" alt="Presenter" />
    </div>
    <div class="text">
        <h1>REMEMBERING THE BEST OF 2022</h1>
        <p>
            Ending 2022 with a bang by remembering the greatest, funniest, sad boi, and definitely
            hottest moments of the year. Have your say by nominating and voting to commemorate your
            favourite moments of this year.
        </p>
    </div>
</div>

<Content />

<!-- Keep at bottom of page -->
<CustomParticles />

<style>
    .desc {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
    }
    img {
        max-width: 100%;
        width: 800px;
        filter: drop-shadow(0px 5px 20px #000);
    }
    .image {
        display: flex;
        padding-right: 29px;
        justify-content: center;
    }
    .text {
        font-size: 20px;
        padding-left: 20px;
    }

    .text h1 {
        font-size: 3em;
        color: rgb(190, 186, 159);
    }

    .text p {
        font-size: 1.25em;
        color: rgb(190, 186, 159);
    }

    @media only screen and (max-width: 700px) {
        .desc {
            flex-direction: column;
        }

        img {
            max-height: 100%;
            height: 400px;
            width: auto;
        }

        .text {
            text-align: center;
        }

        .text h1 {
            font-size: 2em;
        }

        .text p {
            font-size: 1em;
        }
    }
</style>
