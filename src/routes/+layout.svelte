<script>
	// Components
	import Header from '$lib/site/header.svelte';
	import Footer from '$lib/site/footer.svelte';

	// Styles
	import '$lib/global/app.css';

	// Site Data
	const title = 'Cattle Dog Roofing';
	let nav = [
		{
			title: 'About',
			slug: 'about'
		},
		{
			title: 'Contact',
			slug: 'contact'
		},
		{
			title: 'Services',
			slug: 'services'
		}
	];
</script>

<div id="root">
	<Header {title} {nav} />
	<main>
		<slot />
	</main>
	<Footer />
</div>

<style>
	#root {
		position: relative;
		min-height: 100vh;
		padding: 1rem 3rem;
		display: flex;
		flex-flow: column;
		justify-content: space-between;
		gap: 3rem;
		transition: padding 250ms;
	}
	@media (max-width: 500px) {
		#root {
			padding: 1rem;
		}
	}
	main {
		display: flex;
		flex-flow: column;
		gap: 3rem;
	}
</style>
