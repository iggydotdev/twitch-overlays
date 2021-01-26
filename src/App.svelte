<script>
	
	import config from './config/index';
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import VSCode from './VSCode.svelte';
	import Webcam from './Webcam.svelte';
	import Chat from './Chat.svelte';

</script>

<main>

	<Header 
		streamerName={config.header.streamerName} 
		channel={config.header.channel}
		title={config.header.title}
		description={config.header.description}
		topContributor={config.header.topContributor}
	/>

	<section>
		<div class="left-column">
			<VSCode/>
		</div>
		<div class="right-column">
			<Chat />
			<Webcam w={config.webcam.width} h={config.webcam.height} />
		</div>
	</section>
		
	<Footer 
		facebook={config.footer.facebook} 
		youtube={config.footer.youtube}
		twitter={config.footer.twitter}
		song={config.footer.song}
		follower={config.footer.lastFollower}
	/>
	
</main>

<style>
	main {
		text-align: center;
		padding: 0;
		max-width: 240px;
		margin: 0;
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