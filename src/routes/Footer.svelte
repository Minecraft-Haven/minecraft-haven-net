<script>
    import youtube from '$lib/images/youtube.svg';
    import tiktok from '$lib/images/tiktok.svg';
    import instagram from '$lib/images/instagram.svg';
    import twitter from '$lib/images/twitter.svg';
    import twitterx from '$lib/images/x-twitter.svg';
</script>

<header>
    <div class="corner">

    </div>

    <nav>
        <svg style="scale: -1" viewBox="0 0 2 3" aria-hidden="true">
            <path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z"/>
        </svg>
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
        <svg style="scale: -1" viewBox="0 0 2 3" aria-hidden="true">
            <path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z"/>
        </svg>
    </nav>

    <div class="corner">

    </div>
</header>

<style>
    header {
        display: flex;
        justify-content: space-between;
    }

    .corner {
        width: 3em;
        height: 3em;
    }

    nav {
        display: flex;
        justify-content: center;
        --background: rgba(255, 255, 255, 0.7);
    }

    svg {
        width: 2em;
        height: 3em;
        display: block;
    }

    path {
        fill: var(--background);
    }

    ul {
        position: relative;
        padding: 0;
        margin: 0;
        height: 3em;
        display: flex;
        justify-content: center;
        align-items: center;
        list-style: none;
        background: var(--background);
        background-size: contain;
    }

    li {
        position: relative;
        height: 100%;
        padding: 0 1em;
    }

    img {
        color: green;
        width: 1.5em;
    }

    .bluesky {
        width: 1.5em;
        height: 1.5em;
        background-color: blue;
        border-radius: 0.2em;
    }

    nav a {
        display: flex;
        height: 100%;
        align-items: center;
        padding: 0 0.5rem;
        color: var(--color-text);
        font-weight: 700;
        font-size: 0.8rem;
        text-transform: uppercase;
        letter-spacing: 0.1em;
        text-decoration: none;
        transition: color 0.2s linear;
    }

    a:hover {
        color: var(--color-theme-1);
    }
</style>
