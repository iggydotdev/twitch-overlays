<script>
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import config from './config.js';
</script>

<main>

	<Header 
		streamerName={config.streamerName} 
		channel={config.channel}
		title={config.title}
		description={config.description}
		topContributor={config.topContributor}
	/>
	<Footer 
		facebook={config.facebook} 
		youtube={config.youtube}
		twitter={config.twitter}
		nowPlaying={config.song}
		lastFollower={config.lastFollower}
	/>
	
</main>

<style>
	main {
		text-align: center;
		padding: 0;
		max-width: 240px;
		margin: 0;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>