<script lang="ts">
    import Particles from 'svelte-particles';
    import { loadFireworksPreset } from 'tsparticles-preset-fireworks';

    let particlesOptions = {
        preset: 'fireworks',
        sounds: {
            enable: false,
        },
    };

    let particlesInit = async (engine) => {
        await loadFireworksPreset(engine);
    };
</script>

<Particles id="tsparticles" options={particlesOptions} {particlesInit} />
