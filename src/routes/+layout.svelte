<script>
	import Header from '$lib/Header.svelte';
	import '../app.css';
</script>

<svelte:head>
	<title>Ali Hashemi</title>
</svelte:head>

<Header />

<main class="container mx-auto flex flex-col gap-4 p-3">
	<slot />
</main>
