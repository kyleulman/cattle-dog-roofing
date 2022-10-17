<script>
	import Button from './buttons.svelte'

	export let nav

	// * If the width of the window is less than a certain value,
	// * toggle the mobile menu icon on or off
	let mobileMenuIcon = false
	let phoneButton = true
	let windowWidth

	$: {
		windowWidth <= 1024 ? (phoneButton = false) : (phoneButton = true)
		windowWidth <= 768 ? (mobileMenuIcon = true) : (mobileMenuIcon = false)
	}

	// * Keep the mobile menu pane hidden by default
	let mobileMenuPane = false
</script>

<!-- * Watch the width of the window -->
<svelte:window bind:innerWidth="{windowWidth}" />

<header class="small">
	<h1>
		<a href="/">
			<img
				src="/logo.png"
				alt="Cattle Dog Roofing Logo"
				loading="eager"
			/>
		</a>
	</h1>
	<nav class="desktop_menu">
		{#if mobileMenuIcon}
			<!-- * When the menu icon is clicked, set the mobile menu pane to flex -->
			<button
				class="material-icons mobile_menu_icon"
				on:click="{() => (mobileMenuPane = true)}">menu</button
			>
		{:else}
			{#each nav as { title, slug }}<Button
					btnType="center"
					href="{`/${slug}`}"
					text="{title}"
				/>{/each}
		{/if}
	</nav>
	<!-- Only allow the mobile menu pane to appear if the mobile menu icon is showing -->
	{#if mobileMenuIcon}
		<!-- * When anywhere inside the mobile menu pane is clicked, set its display to none -->
		<nav
			class="mobile_menu"
			on:click="{() => (mobileMenuPane = false)}"
			class:show="{mobileMenuPane == true}"
		>
			<div>
				<h2>Jump to page</h2>
				{#each nav as { title, slug }}<Button
						btnType="center"
						href="{`/${slug}`}"
						text="{title}"
					/>{/each}
			</div>
		</nav>
	{/if}
	{#if phoneButton}
		<Button btnType="outline" />
	{/if}
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin: 1em 0;
		gap: 1rem;
	}
	h1 {
		font-size: inherit;
		font-weight: 400;
	}
	.desktop_menu {
		display: flex;
		align-items: center;
		gap: 1rem;
	}
	.mobile_menu {
		display: none;
		justify-content: center;
		align-items: center;
		position: fixed;
		top: 0;
		right: 0;
		bottom: 0;
		left: 0;
		z-index: 2;
		background: var(--clr-dark-transparent);
	}
	.mobile_menu div {
		display: flex;
		flex-flow: column;
		align-items: center;
		gap: 0.5rem;
		text-align: center;
		color: var(--gsl-light);
	}
	.mobile_menu div h2 {
		margin-bottom: 1rem;
	}
	.mobile_menu_icon {
		background: none;
		border: 0;
		font-size: 1.8rem;
		color: var(--clr-primary);
		cursor: pointer;
	}
	a {
		color: inherit;
	}
	a:hover {
		text-decoration: underline;
	}
	.show {
		display: flex;
	}
</style>
