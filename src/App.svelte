<script>
	
	import config from './config/index';
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import Main from './Main.svelte';
</script>

<main>

	<Header 
		streamerName={config.header.streamerName} 
		channel={config.header.channel}
		title={config.header.title}
		description={config.header.description}
		topContributor={config.header.topContributor}
	/>

	<Main />
		
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
		margin: 0;
		height: 90vh;
	}

</style>