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

<Content />

<!-- Keep at bottom of page -->
<CustomParticles />
