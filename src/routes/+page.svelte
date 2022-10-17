<script>
	import Button from '$lib/site/buttons.svelte';

	import Metadata from '$lib/site/metadata.svelte';
	const metadata = {
		title: 'Home',
		description: 'Homepage for Cattle Dog Roofing',
		url: 'https://cattledogroofing.com'
	};
</script>

<Metadata {metadata} />

<section class="content-centered">
	<h2 class="cover">We've got you covered.</h2>
	<p>We install, repair, and replace commercial and residential roofing.</p>
	<div class="hero-cta">
		<Button text="Call Today" />
		<Button btnType="offset" href="/services" text="Learn More" />
	</div>
</section>
<section class="one-two">
	<article class="vert">
		<h3 class="hd-lg">Leaky Roof?</h3>
		<p class="hd hd-sm text-clr-primary">We can help!</p>
		<p>
			Sometimes disaster strikes. You can count on Cattle Dog Roofing to keep your family covered
			when you need it most.
		</p>
	</article>
	<figure>
		<img src="/roof.png" alt="roof" loading="lazy" />
	</figure>
</section>
<section class="space-evenly">
	<figure class="max500">
		<img src="/metal-roof.png" alt="metal roof" loading="lazy" />
	</figure>
	<article class="text-center max500 vert">
		<h3 class="hd-lg">You're Covered</h3>
		<p>
			We offer a wide range of repair and installation options for your residential or commercial
			needs. Ask about our other services, including pressure washing, gutter cleaning, and siding
			installation.
		</p>
		<Button btnType="offset" href="/services" text="Our Services" />
	</article>
</section>
<section class="content-centered">
	<figure class="max900 featured-review">
		<blockquote>
			<p>
				Sean and his crew were awesome! Above and beyond to get a difficult job done. We really
				appreciated his professional job with a personal touch. Lowest quote I received, but we
				could not have had anyone do the job better. SUPER HARD WORKER! Thank you so much Sean for
				taking care of our roof!
			</p>
		</blockquote>
		<figcaption>
			- Karen M on <Button
				btnType="offset"
				href="https://www.facebook.com/CattleDogRoofingLLC/reviews/"
				target="_blank"
				text="Facebook"
			/>
		</figcaption>
	</figure>
</section>
<section class="space-evenly page-cta text-center">
	<h3 class="hd-md max900">
		Call for a <span class="text-clr-primary">FREE</span> quote!
	</h3>
	<Button text="Call Today" />
</section>
<div class="hero-background-top" />
<div class="hero-background-bottom" />

<style>
	.hero-background-top {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		width: 100%;
		padding-bottom: 100%;
		z-index: -1;
		background: linear-gradient(180deg, rgba(34, 34, 34, 0.8), rgba(34, 34, 34, 1) 90%),
			url('/hero-background.png') no-repeat top;
		background-size: cover;
		filter: blur(0.15rem);
	}
	.hero-background-bottom {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		width: 100%;
		padding-top: 100%;
		z-index: -2;
		background: linear-gradient(
				180deg,
				rgba(34, 34, 34, 1) 30%,
				rgba(34, 34, 34, 0.8),
				rgba(34, 34, 34, 1)
			),
			url('/hero-background.png') no-repeat bottom;
		background-size: cover;
		filter: blur(0.15rem);
	}
	.hero-cta {
		display: flex;
		gap: 1rem;
	}
	@media (max-width: 500px) {
		.hero-cta {
			flex-flow: column;
			align-items: center;
			gap: 0.5rem;
		}
	}
	.featured-review {
		background: rgba(34, 34, 34, 0.9);
		box-shadow: 0 0 1rem var(--clr-primary);
		padding: 1rem;
		border-radius: 1rem;
	}
	.page-cta {
		padding: 3rem 0;
		gap: 2rem;
	}
</style>
