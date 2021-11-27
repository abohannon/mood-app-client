<script>
	import { onMount } from 'svelte';

	export let label = '';
	export let reverse = false;

	let value = null;
	$: console.log(label, value);

	let menu = ['Definitely do not feel', 'Do not feel', 'Slightly feel', 'Definitely feel'];

	let score = [1, 2, 3, 4];

	onMount(() => {
		if (reverse) {
			score = score.reverse();
		}
	});
</script>

<h3>{label}</h3>

<div class="likert">
	{#each menu as item, i}
		<label>
			<input name="likert" type="radio" bind:group={value} value={score[i]} />
			<span>{item}</span>
		</label>
	{/each}
</div>

<style>
	.likert {
		display: flex;
	}

	.likert input {
		max-width: 250px;
	}
</style>
