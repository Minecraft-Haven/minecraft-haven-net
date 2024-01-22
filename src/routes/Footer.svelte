<script>
    import youtube from '$lib/images/youtube.svg';
    import tiktok from '$lib/images/tiktok.svg';
    import instagram from '$lib/images/instagram.svg';
    import twitter from '$lib/images/twitter.svg';
    import twitterx from '$lib/images/x-twitter.svg';
</script>

<footer>
    <ul>
        <li>
            <a href="https://www.youtube.com/channel/UC1LKNodmraOQZV81x7qnebg" target="_blank">
                <img src={youtube} alt="YouTube"/></a>
        </li>
        <li>
            <a href="https://www.tiktok.com/@melonpanoffical?lang=en" target="_blank">
                <img src={tiktok} alt="TikTok"/></a>
        </li>
        <li>
            {#if Math.random() > 0.5}
                <a href="https://twitter.com/melonpanoffice" target="_blank">
                    <img src={twitter} alt="Twitter"/></a>
            {:else}
                <a href="https://x.com/melonpanoffice" target="_blank">
                    <img src={twitterx} alt="X"/></a>
            {/if}
        </li>
        <li>
            <a href="https://www.instagram.com/melonpanoffice/" target="_blank">
                <img src={instagram} alt="Instagram"/></a>
        </li>
        <li>
            <a href="https://bsky.app/profile/melonpanofficial.bsky.social" target="_blank">
                <div class="bluesky"></div>
            </a>
        </li>
    </ul>
    <p style="color: grey; margin-top: auto; font-size: 0.5rem;">DISCLAIMER: melonpan is not associated with Microsoft, Mojang, or Minecraft in any way.</p>
</footer>

<style>
    footer {
        position: absolute;
        bottom: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 10vh;
        overflow: hidden;
        justify-content: space-between;
        padding-top: 0.5rem;
        --background: rgba(255, 255, 255, 0.7);
        background: var(--background);
    }

    ul {
        display: flex;
        width: 100%;
        height: 6rem;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        position: relative;
        padding: 0;
        margin: 0;
        list-style: none;
        background-size: contain;
    }

    li {
        position: relative;
        height: 100%;
        padding: 0 1rem;
    }

    img {
        color: green;
        width: 1.5rem;
    }

    .bluesky {
        width: 1.5rem;
        height: 1.5rem;
        background-color: blue;
        border-radius: 0.2rem;
    }

    a {
        display: flex;
        height: 100%;
        align-items: center;
        padding: 0 0.5rem;
        color: var(--color-text);
        font-weight: 700;
        font-size: 0.8rem;
        text-transform: uppercase;
        letter-spacing: 0.1rem;
        text-decoration: none;
        transition: color 0.2s linear;
    }

    a:hover {
        color: var(--color-theme-1);
    }
</style>
