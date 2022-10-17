<script>
	export let metadata = {}

	export const defaults = {
		title: 'Cattle Dog Roofing',
		description:
			'We install, repair, and replace commercial and residential roofing.',
		image_alt: 'Cattle Dog Roofing LLC',
		url: 'https://www.cattledogroofing.com',
		type: 'website',
		twitter_card: 'summary_large_image',
		app_id: ''
	}
</script>

<svelte:head>
	{#if metadata.title}
		<title>{metadata.title} - {defaults.title}</title>
		<meta
			name="title"
			content="{`${metadata.title} - ${defaults.title}`}"
		/>
		<meta
			property="og:title"
			content="{`${metadata.title} - ${defaults.title}`}"
		/>
		<meta
			property="twitter:title"
			content="{`${metadata.title} - ${defaults.title}`}"
		/>
	{:else}
		<title>{defaults.title}</title>
		<meta name="title" content="{defaults.title}" />
		<meta property="og:title" content="{defaults.title}" />
		<meta property="twitter:title" content="{defaults.title}" />
	{/if}

	{#if metadata.description}
		<meta
			name="description"
			content="{`${metadata.description} — ${defaults.description}`}"
		/>
		<meta
			property="og:description"
			content="{`${metadata.description} — ${defaults.description}`}"
		/>
		<meta
			property="twitter:description"
			content="{`${metadata.description} — ${defaults.description}`}"
		/>
	{:else}
		<meta name="description" content="{defaults.description}" />
		<meta property="og:description" content="{defaults.description}" />
		<meta property="twitter:description" content="{defaults.description}" />
	{/if}

	{#if metadata.image}
		<meta property="og:image" content="{metadata.image}" />
		<meta property="twitter:image" content="{metadata.image}" />
	{:else}
		<meta property="og:image" content="{defaults.image}" />
		<meta property="twitter:image" content="{defaults.image}" />
	{/if}

	{#if metadata.image_alt}
		<meta property="og:image:alt" content="{metadata.image_alt}" />
		<meta property="twitter:image:alt" content="{metadata.image_alt}" />
	{:else}
		<meta property="og:image:alt" content="{defaults.image_alt}" />
		<meta property="twitter:image:alt" content="{defaults.image_alt}" />
	{/if}

	{#if metadata.url}
		<meta property="og:url" content="{metadata.url}" />
		<meta property="twitter:url" content="{metadata.url}" />
	{:else}
		<meta property="og:url" content="{defaults.url}" />
		<meta property="twitter:url" content="{defaults.url}" />
	{/if}

	<meta property="og:type" content="{defaults.type}" />

	<meta property="fb:app_id" content="{defaults.app_id}" />

	{#if metadata.twitter_card}
		<meta property="twitter:card" content="{metadata.twitter_card}" />
	{:else}
		<meta property="twitter:card" content="{defaults.twitter_card}" />
	{/if}
</svelte:head>
