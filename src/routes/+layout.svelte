<script lang="ts">
	import Header from '../lib/components/Header.svelte';
	import '../app.css';
	import 'bootstrap/dist/css/bootstrap.min.css';
	
  	import { onMount } from 'svelte';

	onMount(async () => {
		if (typeof window !== 'undefined') {
			await import('bootstrap/dist/js/bootstrap.min.js');
		}
	});

</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}


	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
