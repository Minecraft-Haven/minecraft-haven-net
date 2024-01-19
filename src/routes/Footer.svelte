<script>
    import youtube from '$lib/images/youtube.svg';
    import tiktok from '$lib/images/tiktok.svg';
    import instagram from '$lib/images/instagram.svg';
    import twitter from '$lib/images/twitter.svg';
    import twitterx from '$lib/images/x-twitter.svg';
</script>

<footer>
    <nav>
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
        <p>DISCLAIMER: melonpan is not associated with Microsoft, Mojang, or Minecraft in any way.</p>
    </nav>
</footer>

<style>
    footer {
        display: flex;
        width: 100%;
        height: 6rem;
        justify-content: space-between;
    }

    nav {
        display: flex;
        width: 100vw;
        height: 6rem;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        --background: rgba(255, 255, 255, 0.7);
        background: var(--background);
    }

    ul {
        position: relative;
        padding: 0;
        margin: 0;
        width: 100vw;
        height: 6rem;
        display: flex;
        justify-content: center;
        align-items: center;
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

    nav a {
        display: flex;
        height: 4rem;
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
