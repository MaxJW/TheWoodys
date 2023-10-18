<script lang="ts">
    function scrollIntoView({ target }) {
        const el = document.querySelector(target.getAttribute('href'));
        if (!el) return;
        el.scrollIntoView({
            behavior: 'smooth',
        });
    }
</script>

<div class="desc">
    <div class="image">
        <img src="images/presenter.png" alt="Presenter" />
    </div>
    <div class="text">
        <h1>REMEMBERING THE BEST OF 2023</h1>
        <p>
            Ending 2023 with a bang by remembering the greatest, funniest, sad boi, and definitely
            hottest moments of the year. Have your say by nominating and voting to commemorate your
            favourite moments of this year.<br />Voting is not yet open.
        </p>
        <a href="https://docs.google.com/forms/d/1-7Kfi1XeTSgT9Uwy-ZuBAnby1zi0Wf9SFEzML7QLVUI">
            <input type="button" value="Vote Here" id="vote-button" disabled />
        </a>
    </div>
</div>

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
</style>
