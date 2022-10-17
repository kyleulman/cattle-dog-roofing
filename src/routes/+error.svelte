<article>
	<h2 class="cover">Page Not Found</h2>
	<p>
		Click <button class="center" on:click={() => history.back()}>here</button> to go back
	</p>
</article>

<style>
	button {
		display: inline;
		position: relative;
		padding: 0.5rem 1rem;
		text-decoration: none;
		border-radius: 0.25rem;
		font-weight: 500;
		white-space: nowrap;
		cursor: pointer;
		background: none;
		font-family: inherit;
		font-size: inherit;
		border: none;
	}
	.center {
		color: var(--clr-light);
		padding: 0.5rem 0;
	}
	.center::after {
		content: '';
		position: absolute;
		width: 70%;
		left: 50%;
		transform: translateX(-50%);
		bottom: 0.25rem;
		border-bottom: 0.2rem solid var(--clr-primary-light);
		opacity: 0.8;
		transition: width 250ms;
	}
	.center:hover::after {
		width: 100%;
		border-bottom: 0.2rem solid var(--clr-primary);
	}
</style>
