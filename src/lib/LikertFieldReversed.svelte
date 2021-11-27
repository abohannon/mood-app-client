<script>
	export let label;

	let value = null;
	$: console.log('value', value);

	let menu = [
		{ label: 'Definitely do not feel', value: 4 },
		{ label: 'Do not feel', value: 3 },
		{ label: 'Slightly feel', value: 2 },
		{ label: 'Definitely feel', value: 1 }
	];
</script>

<h3>
	{label}
</h3>
<div class="likert">
	{#each menu as item}
		<label>
			<input name="likert-reversed" type="radio" bind:group={value} value={item.value} />
			<span>{item.label}</span>
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
