<script>
	import Metadata from '$lib/site/metadata.svelte';
	const metadata = {
		title: 'About Us',
		description: 'About Cattle Dog Roofing',
		url: 'https://cattledogroofing.com/about'
	};

	const about = {
		heading: 'About Us',
		body: `Cattle Dog Roofing LLC is owned an operated by Sean and Kinsley Tate. They live in the New River Valley with their dogs, Luna and Chance.`,
		image: {
			src: '/kinsley-sean.png',
			alt: 'Kinsley and Sean'
		}
	};
</script>

<Metadata {metadata} />
<h2 class="cover">{about.heading}</h2>
<section class="about_main one-one">
	<article>
		{@html about.body}
	</article>
	{#if about.about_image !== null}
		<figure>
			<img src={about.image.src} alt={about.image.alt} class="about_image" />
		</figure>
	{/if}
</section>
<section class="about_footer one-one">
	<figure>
		<img src="/luna-ladder.jpg" alt="Luna up a ladder" />
	</figure>
	<div>
		<article class="vert">
			<p>
				Have you ever heard of a dog that enjoys climbing ladders? One day Sean was working on a
				project at our home when our Australian cattle dog Luna started climbing his ladder. Once
				Luna discovered the joy of climbing, she started going up every ladder in sight. The name
				Cattle Dog Roofing was inspired by our pup Luna and pays tribute to the popular breed in the
				southwest Virginia area.
			</p>
			<p>— Kinsley</p>
		</article>
		<figure>
			<img class="about_image" src="/luna-smile-cropped.png" alt="Luna smiling" />
		</figure>
	</div>
</section>

<style>
	section {
		max-width: 1024px;
		margin: auto;
	}
	.about_main:nth-child(even) > figure {
		order: 1;
	}
	.about_main:nth-child(odd) > article {
		order: 2;
	}
	.about_image {
		border-radius: 50%;
		width: 600px;
	}
	.about_footer {
		align-items: flex-start;
	}
	.about_footer > div {
		display: flex;
		flex-flow: column;
		align-items: center;
		gap: 1rem;
	}
	@media (max-width: 1200px) {
		.about_footer > div > article {
			order: 2;
		}
		.about_footer > div > figure {
			order: 1;
		}
	}
</style>
