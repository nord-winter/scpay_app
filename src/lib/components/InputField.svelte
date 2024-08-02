<script lang="ts">
	export let value: string;
	export let label: string;
	export let type: string = 'text';

	function typeAction(node: HTMLInputElement): void {
		node.type = type;
	}
</script>

<p class="form-control">
	{#if label}
		<label class="label" for="{label}">{label}:</label>
	{/if}
	<input id="{label}" use:typeAction class="input" bind:value={value}/>
</p>

<style>
	.form-control {
		margin: .5rem 0;
		text-align: left;
	}
	.input {
		width: 100%;
		display: block;
		padding: 0.5rem 0;
		margin-top: 0.5rem;
		border-width: 1px;
		border-radius: 0.25rem;
		background-color: bisque;
	}
	.label {
		color: gray;
	}
</style>
