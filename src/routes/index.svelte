<script context="module">
	import { goto } from '$app/navigation';
	export const prerender = true;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<h1>How are you feeling today?</h1>
	<button on:click={() => goto('/mood')}>Start</button>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}
</style>
