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
	<div class="tiles">
		<div class="announcements">
			<h2 style="text-align: center;">Announcements</h2>
			<p>
				Server launches this Friday!
			</p>
		</div>
		<div class="ip">
			<h1>melonpan</h1>
			<h2>A Minecraft Minigame Server</h2>
			Play below {timeDisplay}
			<pre title="copy to clipboard" on:keypress={(key) => key.key === 'Enter' && navigator.clipboard.writeText('melonpan.xyz')} on:click={() => navigator.clipboard.writeText('melonpan.xyz')}>melonpan.xyz</pre>
		</div>
		<div class="rules">
			<h2 style="text-align: center;">Server Rules</h2>
			<ol>
				<li>Use common sense.</li>
				<li>Don't be malicious.</li>
				<li>Jokes are funny twice, not three times.</li>
				<li>melonpan</li>
				<li>melonpan</li>
				<li>melonpan</li>
			</ol>
		</div>
	</div>
</section>

<style>
	section {
		display: flex;
		height: 100%;
		overflow: hidden;
	}

	h1 {
		width: 100%;
		font-size: 3.5rem;
		margin-bottom: 0;
	}

	h2 {
			font-size: 1.5rem;
	}

	.tiles {
			flex: 1;
			display: grid;
			grid-template-columns: 1fr 2fr 1fr;
			grid-template-rows: 1fr;
	}

	@media(max-width: 768px) {
			.tiles {
					grid-template-columns: 1fr;
			}
			.rules {
					display: none;
			}
			.announcements {
					display: none;
			}
  }

	.ip {
		margin-top: 2em;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.rules {
      border-radius: 5px;
      background: rgba(255, 255, 255, 0.5);
	}

	.announcements {
			padding: 1rem;
			border-radius: 5px;
			background: rgba(255, 255, 255, 0.5);
	}

	.rules li {
			margin: 0.5rem;
	}

	pre {
		margin-top: 0.3rem;
		background: rgba(0, 0, 0, 0.5);
		color: white;
			font-size: 1.5rem;
	}
</style>
