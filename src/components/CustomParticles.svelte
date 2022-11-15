<script lang="ts">
    import Particles from 'svelte-particles';
    import { loadFull } from 'tsparticles';

    const p = {
        fpsLimit: 165,
        emitters: {
            direction: 'top',
            size: {
                width: 100,
                height: 0,
            },
            position: {
                x: 50,
                y: 100,
            },
            rate: {
                delay: 0.1,
                quantity: 2,
            },
        },
        particles: {
            number: {
                value: 0,
                density: {
                    enable: true,
                    value_area: 200,
                },
            },
            color: {
                value: ['#faffa1', '#b98c4b'],
            },
            shape: {
                type: 'circle',
                stroke: {
                    width: 0,
                    color: '#000000',
                },
            },
            opacity: {
                value: 1,
                random: true,
                anim: {
                    enable: false,
                    speed: 3,
                    opacity_min: 0.1,
                    sync: false,
                },
            },
            size: {
                value: 10,
                random: false,
                anim: {
                    enable: true,
                    speed: 5,
                    size_min: 0.1,
                    sync: true,
                    startValue: 'min',
                    destroy: 'max',
                },
            },
            line_linked: {
                enable: false,
            },
            move: {
                enable: true,
                speed: 5,
                direction: 'none',
                random: false,
                straight: false,
                out_mode: 'destroy',
                attract: {
                    enable: false,
                    rotateX: 600,
                    rotateY: 1200,
                },
            },
        },
    };

    let particlesInit = async (engine) => {
        await loadFull(engine);
    };
</script>

<Particles id="tsparticles" options={p} {particlesInit} />
