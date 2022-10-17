<script>
	const year = new Date().getFullYear()
</script>

<footer class="bd-sm">
	<section class="top">
		<div class="info-block">
			<span class="material-icons">schedule</span>
			<div>
				<p>Monday-Saturday<br />7:00am-7:00pm</p>
				<p><i>Closed on Sunday</i></p>
			</div>
		</div>
		<a href="/contact#contact-map" class="info-block">
			<span class="material-icons">place</span>
			<div>
				<p>We serve the New River Valley area</p>
				<p><u>Service Map</u></p>
			</div>
		</a>
		<a href="tel:910-619-1682" class="info-block">
			<span class="material-icons">phone</span>
			<div>
				<p>Call to book an appointment</p>
				<p><u>910-619-1682</u></p>
			</div>
		</a>
	</section>

	<section class="space-between mid">
		<p>
			Cattle Dog Roofing LLC is licensed & insured (<a
				href="https://www.thumbtack.com/va/blacksburg/roofing/cattle-dog-roofing-llc/service/399751913764323336"
				target="_blank">#2705175065</a
			>)
		</p>
	</section>

	<section class="bottom">
		<div>
			<span>&copy;</span>
			{year} Cattle Dog Roofing
		</div>
		<div class="social-links">
			<span class="material-icons socials"
				><a href="tel:9106191682">phone</a></span
			>
			<span class="material-icons socials"
				><a href="/contact#contact-information">email</a></span
			>
			<span class="material-icons socials"
				><a
					href="https://facebook.com/CattleDogRoofingLLC"
					target="_blank">facebook</a
				></span
			>
			<span class="material-icons socials"
				><a
					href="https://google.com/search?q=cattle+dog+roofing"
					target="_blank">storefront</a
				></span
			>
		</div>
	</section>
</footer>

<style>
	footer {
		display: flex;
		flex-flow: column;
		gap: 1rem;
	}
	.top {
		display: flex;
		flex-flow: row wrap;
		justify-content: space-between;
		align-items: center;
		gap: 1rem;
	}
	.info-block {
		position: relative;
		display: flex;
		align-items: center;
		gap: 1rem;
		padding: 1rem;
		background: var(--clr-dark-1);
		border-radius: 0.25rem;
		text-decoration: none;
		flex: 1;
		min-height: 168px;
		min-width: 330px;
		transition: background 250ms;
	}
	a.info-block:hover {
		background: var(--clr-dark-2);
	}
	.info-block > span {
		font-size: 2em;
		color: var(--clr-primary);
	}
	.info-block > div {
		display: flex;
		flex-flow: column;
		gap: 0.5rem;
	}
	.info-block > div > :first-child {
		font-size: 1.5em;
		font-weight: 700;
	}
	@media (max-width: 600px) {
		.info-block {
			flex-flow: column;
			align-items: center;
			text-align: center;
			flex: 1;
			min-width: 100%;
		}
	}

	@media (max-width: 1200px) {
		.mid {
			flex-flow: column;
			gap: 1em;
			text-align: center;
		}
	}

	.bottom {
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 1rem;
	}
	@media (max-width: 768px) {
		.bottom {
			flex-flow: column;
			text-align: center;
		}
		.bottom > :nth-child(1) {
			order: 3;
		}
		.bottom > :nth-child(2) {
			order: 1;
		}
		.bottom > :nth-child(3) {
			order: 2;
		}
	}
	.social-links {
		display: flex;
		gap: 1em;
	}
	.socials {
		position: relative;
	}
	.socials:after {
		content: '';
		position: absolute;
		width: 50%;
		height: 50%;
		top: 50%;
		left: 50%;
		z-index: -1;
		transform: translate(-50%, -50%);
		background: var(--clr-primary);
		border-radius: 100%;
		transition: 250ms;
	}
	.socials:hover::after {
		width: 130%;
		height: 130%;
	}
	.socials a {
		text-decoration: none;
	}
</style>
