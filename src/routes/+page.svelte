<script>
	import { onMount } from 'svelte';

	let time = (Date.UTC(2024, 0, 19, 17) - Date.now()) / 1000;
	let timeDisplay = '';
	let hours, minutes, seconds;

	onMount(() => {
		setInterval(() => time = (Date.UTC(2024, 0, 19, 17) - Date.now()) / 1000, 1000);
	});

	$: {
		hours = Math.floor((time / 3600));
		minutes = Math.floor(time % 3600 / 60);
		seconds = Math.floor(time % 60);
		timeDisplay = time > 0 ? `in ${hours >= 10 ? hours : `0${hours}`}:${minutes >= 10 ? minutes : `0${minutes}`}:${seconds >= 10 ? seconds : `0${seconds}`}` : 'now';
	}
</script>

<svelte:head>
	<title>melonpan</title>
	<meta name="description" content="melonpan" />
</svelte:head>

<section>
	<h1>melonpan</h1>
	<h2>A Minecraft Survival Server</h2>

	<div class="tiles">
		<div class="ip">
			Play below {timeDisplay}
			<pre title="copy to clipboard" on:keypress={(key) => key.key === 'Enter' && navigator.clipboard.writeText('melonpan.xyz')} on:click={() => navigator.clipboard.writeText('melonpan.xyz')}>melonpan.xyz</pre>
		</div>
		<div class="announcements"></div>
		<div class="rules"></div>
		<div class="faq"></div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		margin-bottom: 0;
	}

	div {
		margin-top: 2em;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	pre {
		margin-top: 0.3em;
		background: rgba(0, 0, 0, 0.5);
		color: white;
			font-size: 1.5rem;
	}
</style>
