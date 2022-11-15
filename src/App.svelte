<script lang="ts">
    import Blur from './components/Blur.svelte';
    import Content from './components/Content.svelte';
    import CustomParticles from './components/CustomParticles.svelte';
    import Heading from './components/Heading.svelte';
</script>

<Heading />
<!-- Anything above will never be blurred -->

<Blur />

<Content />

<!-- Keep at bottom of page -->
<CustomParticles />
