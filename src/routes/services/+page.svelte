<script>
	const services = [
		{
			heading: 'Metal Roofing',
			body: 'We install 26 and 29 gauge agricultural panels also known as screw down or exposed fastener metal roofs. Another popular option that we install are standing seam metal roof panels which are often 24 gauge and 26 gauge with no trim or panels having any fasteners exposed. A cleat system is used to get this result which increases the maintenance free life of the roof. There are other options available as well as R panels, insulated panel varieties, and corrugated panels.',
			image: {
				src: '/metal-icon.png',
				alt: 'Metal roofing.'
			}
		},
		{
			heading: 'Shingle Roofing',
			body: 'We mainly install architectural asphalt shingles as they offer better durability than the 3 tab variety. All installations are fully torn off before replacement and all shingles are 6 nailed and all cap shingles are 4 nailed helping to prevent future blow off. An ice and water barrier is installed to eaves and valleys to prevent ice damming (full roof coverage when less than 4/12 pitch).',
			image: {
				src: '/shingle-icon.png',
				alt: 'Shingle roofing.'
			}
		},
		{
			heading: 'Single-Ply Roofing',
			body: 'We install EPDM (rubber) and TPO (thermoplastic) roofing for many low slope applications. The standard polyiso-insulation and taper base is customized for each situation to maintain warmth and drainage.',
			image: {
				src: '/single-ply-icon.png',
				alt: 'Single-ply roofing.'
			}
		},
		{
			heading: 'Other Services',
			body: `<ul><li>Soffit, fascia, chimney flashing</li><li>Gutter cleaning</li><li>Pressure washing</li><li>Framing repairs (sagging floor, broken rafter, rotten joist, leaning deck)</li></ul>`,
			image: {
				src: '/weathering-icon.png',
				alt: 'Other services.'
			}
		}
	];

	import Metadata from '$lib/site/metadata.svelte';
	const metadata = {
		title: 'Our Services',
		description: 'Cattle Dog Roofing Services',
		url: 'https://cattledogroofing.com/services'
	};
</script>

<Metadata {metadata} />
<h2 class="cover">Our Services</h2>
{#each services as service}
	<article>
		<figure class="header">
			<img src={service.image.src} alt={service.image.alt} />
			<figcaption>
				<p class="hd-sm">{service.heading}</p>
			</figcaption>
		</figure>
		<div class="content">
			{@html service.body}
		</div>
	</article>
{/each}

<style>
	article {
		max-width: 1024px;
		margin: auto;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 2rem;
	}
	@media (max-width: 1024px) {
		article {
			flex-flow: column;
			gap: 1rem;
		}
	}
	article > .header {
		display: flex;
		flex-flow: column;
		align-items: center;
		text-align: center;
		max-width: 200px;
		gap: 0.5rem;
	}
	article > .content {
		flex: 1;
	}
	figcaption {
		text-align: center;
		font-style: normal;
		font-weight: 700;
		color: var(--clr-primary);
	}
</style>
