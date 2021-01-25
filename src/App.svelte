<script>
	
	import config from './config.js';
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import VSCode from './VSCode.svelte';
	import Webcam from './Webcam.svelte';
	import Chat from './Chat.svelte';
</script>

<main>

	<Header 
		streamerName={config.streamerName} 
		channel={config.channel}
		title={config.title}
		description={config.description}
		topContributor={config.topContributor}
	/>

	<section>
		<div class="left-column">
			<VSCode/>
		</div>
		<div class="right-column">
			<Chat/>
			<Webcam/>
		</div>
	</section>
		
	<Footer 
		facebook={config.facebook} 
		youtube={config.youtube}
		twitter={config.twitter}
		song={config.song}
		follower={config.lastFollower}
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


	section {
		display: flex;
		flex-flow: row nowrap;
		justify-content: center;
	}

	.left-column {
		width: 100%;
	}
	.right-column {
		width: 320px;
		display: flex;
		flex-flow: column nowrap;
	}
</style>