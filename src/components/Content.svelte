<script lang="ts">
    function scrollIntoView({ target }) {
        const el = document.querySelector(target.getAttribute('href'));
        if (!el) return;
        el.scrollIntoView({
            behavior: 'smooth',
        });
    }
</script>

<p class="sponsor">Sponsored by Young Sheldon</p>
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
        <a href="https://forms.gle/vKjhQVEcyeMRdeJ59">
            <input type="button" value="Vote Here" id="vote-button" />
        </a>
    </div>
</div>

<!-- <div class="content" id="form">
    <iframe
        title="The Woodys Form"
        src="https://docs.google.com/forms/d/e/1FAIpQLSeyn7ZxSpbLs4-eDjLKtx-Ph4P5NK8-XB6BPo-oxf0U0f-9Ew/viewform?embedded=true"
        width="100%"
        height="100%"
        frameborder="0"
        marginheight="0"
        marginwidth="0">Loading…</iframe
    >
</div> -->
<style>
    .sponsor {
        text-align: center;
        color: #beba9f;
        z-index: 10;
    }

    .desc {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        z-index: 10;
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
        z-index: 10;
    }

    .text {
        font-size: 20px;
        padding-left: 20px;
        z-index: 10;
    }

    .text h1 {
        font-size: 3em;
        color: rgb(190, 186, 159);
    }

    .text p {
        font-size: 1.25em;
        color: rgb(190, 186, 159);
    }

    #vote-button {
        background-color: #1b1b1b;
        border: 1px solid #bdb9a1;
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
            display: flex;
            flex-direction: column;
            padding-left: 0;
            min-height: 65vh;
        }

        .text h1 {
            font-size: 2em;
        }

        .text p {
            font-size: 1em;
        }

        a {
            max-width: 50%;
            align-self: center;
        }
    }

    .content {
        position: relative;
        z-index: 1;
        margin-top: 4em;
        scroll-margin: 5vh;
        z-index: 10;
    }

    .content iframe {
        min-height: 3000px;
        border-radius: 8px;
    }
</style>
