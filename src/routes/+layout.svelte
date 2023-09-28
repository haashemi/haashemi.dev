<script>
	import Header from '$lib/Header.svelte';
	import { onMount } from 'svelte';
	import '../app.css';

	onMount(() => {
		console.log('%c ----------------', 'font-size: 30px;');
		console.log('%c BRO HIRE ME NOW!', 'font-size: 50px; font-style: italic;');
		console.log('%c contact@haashemi.dev', 'font-style: italic;');
		console.log('%c https://github.com/haashemi', 'font-style: italic;');
		console.log('%c ----------------', 'font-size: 30px;');
	});
</script>

<svelte:head>
	<title>Ali Hashemi</title>
	<meta name="description" content="Ali Hashemi's portfolio website." />
</svelte:head>

<main class="min-h-screen w-full bg-black">
	<div class="container mx-auto flex flex-col gap-4 p-3">
		<Header />

		<slot />
	</div>
</main>
