<script>
	import Counter from '$lib/components/Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import MultiStepForm from '$lib/components/MultiStepForm.svelte';
	import Cards from '../lib/components/Cards.svelte';
	import Hero from '$lib/components/Hero.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<!-- <h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2> -->

	<div class="container text-center bg-body-tertiary">
		<div class="col-md-6 p-lg-5 mx-auto my-5">
		<h1 class="display-3 fw-bold">Designed for engineers</h1>
		<h3 class="fw-normal text-muted mb-3">Build anything you want with Aperture</h3>
		<div class="d-flex gap-3 justify-content-center lead fw-normal">
			<!-- svelte-ignore a11y-invalid-attribute -->
			<a class="icon-link" href="#">
			Learn more
			<svg class="bi"><use xlink:href="#chevron-right"></use></svg>
			</a>
			<!-- svelte-ignore a11y-invalid-attribute -->
			<a class="icon-link" href="#">
			Buy
			<svg class="bi"><use xlink:href="#chevron-right"></use></svg>
			</a>
		</div>
		</div>
	</div>
</section>

<section>
	<div class="container">
		<div class="d-flex flex-column flex-md-row gap-4 pt-5 align-items-center justify-content-around">
			<Counter />
			<MultiStepForm />
		</div>
	</div>
</section>

<Cards />

<Hero />

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	/* h1 {
		width: 100%;
	} */

	/* .welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	} */
</style>
