<script>
	import LikertField from '$lib/LikertField.svelte';
</script>

<svelte:head>
	<title>My Mood</title>
</svelte:head>

<div>
	<form>
		<LikertField label="Active" />
		<LikertField label="Calm" />
		<LikertField label="Caring" />
		<LikertField label="Content" />
		<LikertField label="Happy" />
		<LikertField label="Lively" />
		<LikertField label="Loving" />
		<LikertField label="Peppy" />
		<LikertField reverse label="Drowsy" />
		<LikertField reverse label="Fed up" />
		<LikertField reverse label="Gloomy" />
		<LikertField reverse label="Grouchy" />
		<LikertField reverse label="Jittery" />
		<LikertField reverse label="Nervous" />
		<LikertField reverse label="Sad" />
		<LikertField reverse label="Tired" />
	</form>
</div>
