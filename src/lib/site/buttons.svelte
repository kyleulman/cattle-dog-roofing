<script>
	export let btnType = 'solid';
	export let href = 'tel:910-619-1682';
	export let target = '';
	export let text = '910-619-1682';
	export let btnOnClick = '';

	let btnClass = 'solid';

	if (btnType == 'outline') {
		btnClass = 'outline';
	}

	if (btnType == 'center') {
		btnClass = 'center';
	}

	if (btnType == 'offset') {
		btnClass = 'offset';
	}

	if (btnType == 'block') {
		btnClass = 'block';
	}
	if (btnType == 'left') {
		btnClass = 'left';
	}
</script>

<a {href} {target} on:click={btnOnClick} class={btnClass}>{text}</a>

<style>
	a {
		display: inline;
		position: relative;
		padding: 0.5rem 1rem;
		text-decoration: none;
		border-radius: 0.25rem;
		font-weight: 500;
	}
	@media (max-width: 400px) {
		a {
			overflow-wrap: break-word;
			word-break: break-word;
			/* Adds a hyphen where the word breaks, if supported (No Blink) */
			-ms-hyphens: auto;
			-moz-hyphens: auto;
			-webkit-hyphens: auto;
			hyphens: auto;
		}
	}
	.outline {
		color: var(--clr-primary);
		border: 1px solid var(--clr-primary);
		transition: background 250ms, color 250ms;
		text-transform: uppercase;
	}
	.outline:hover {
		background: var(--clr-primary);
		color: var(--clr-light);
	}

	.solid {
		color: var(--clr-light);
		border: 1px solid var(--clr-primary);
		background: var(--clr-primary);
		transition: 250ms;
		text-transform: uppercase;
	}
	.solid:hover {
		box-shadow: 0 0 1rem var(--clr-primary-light);
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

	.left {
		color: var(--clr-light);
		padding: 0.5rem 0;
	}
	.left::after {
		content: '';
		position: absolute;
		width: 70%;
		left: 0;
		bottom: 0.25rem;
		border-bottom: 0.2rem solid var(--clr-primary-light);
		opacity: 0.8;
		transition: width 250ms;
	}
	.left:hover::after {
		width: 100%;
		border-bottom: 0.2rem solid var(--clr-primary);
	}

	.offset {
		position: relative;
		color: var(--clr-light);
		padding: 0.5rem 0;
	}
	.offset::after {
		content: '';
		position: absolute;
		width: 75%;
		right: -0.5rem;
		bottom: 0.25rem;
		border-bottom: 0.2rem solid var(--clr-primary-light);
		opacity: 0.8;
		transition: transform 250ms;
	}
	.offset:hover::after {
		transform: translateX(0.5rem);
		border-bottom: 0.2rem solid var(--clr-primary);
	}

	.block {
		/* outline: 1px solid red; */
		width: 100%;
		text-align: center;
		color: var(--clr-primary);
		background: var(--clr-dark-0);
	}
	.block:hover {
		background: var(--clr-dark-2);
	}
</style>
