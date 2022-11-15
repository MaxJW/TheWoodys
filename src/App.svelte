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
<p style="text-align: center; color: #beba9f;">Sponsored by Young Sheldon</p>
<!-- Keep at bottom of page -->
<CustomParticles />
