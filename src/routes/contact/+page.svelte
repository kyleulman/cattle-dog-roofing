<script>
	import Button from '$lib/site/buttons.svelte';
	import Metadata from '$lib/site/metadata.svelte';

	const metadata = {
		title: 'Contact Us',
		description: 'Contact Cattle Dog Roofing',
		url: 'https://cattledogroofing.com/contact'
	};
</script>

<Metadata {metadata} />

<h2 class="cover">Contact Us</h2>
<section class="space-evenly contact-info">
	<article id="contact-information">
		<ul>
			<li>
				<span class="material-icons">phone</span>
				<Button href="tel:9106191682" text="910-619-1682" btnType="left" />
			</li>
			<li>
				<span class="material-icons">mail</span><Button
					href="mailto:cattledogroofing@gmail.com"
					text="cattledogroofing@gmail.com"
					btnType="left"
				/>
			</li>
			<li>
				<span class="material-icons">place</span><Button
					href="https://goo.gl/maps/WdLarbVtBma9avm78"
					target="_blank"
					btnType="left"
					text="New River Valley Area"
				/>
			</li>
			<li>
				<span class="material-icons">facebook</span><Button
					href="https://www.facebook.com/CattleDogRoofingLLC/"
					target="_blank"
					text="@cattledogroofingllc"
					btnType="left"
				/>
			</li>
		</ul>
	</article>
	<figure>
		<img src="/luna-cropped.png" alt="luna" loading="eager" />
		<figcaption>Our pup, Luna, namesake of the company</figcaption>
	</figure>
</section>
<section class="contact-map" id="contact-map">
	<iframe
		src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d406806.7789811412!2d-80.36320435156246!3d37.19600231044778!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x54254a53c80a577d!2sCattle%20Dog%20Roofing%20LLC!5e0!3m2!1sen!2sus!4v1627021301755!5m2!1sen!2sus"
		loading="lazy"
		title="our service area"
	/>
</section>

<style>
	@media (max-width: 500px) {
		.contact-info {
			align-items: flex-start;
		}
	}
	figure {
		max-width: 600px;
	}

	img {
		border-radius: 100%;
		box-shadow: 0 0 0.25rem var(--clr-primary);
	}

	ul {
		padding-left: 0;
		list-style: none;
	}
	li {
		display: flex;
		align-items: center;
		margin: 1rem 0;
	}
	li::before {
		content: '';
	}
	@media (max-width: 500px) {
		li {
			flex-flow: column;
			align-items: flex-start;
		}
	}
	li span {
		font-size: 2em;
		color: var(--clr-primary);
		margin-right: 1rem;
	}
	.contact-map > * {
		width: 100%;
		height: 500px;
		border: none;
		border-radius: 0.25rem;
	}
</style>
