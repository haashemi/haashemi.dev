<script>
	import Header from '$lib/Header.svelte';
	import '../app.css';

	console.log('%c ----------------', 'font-size: 30px;');
	console.log('%c BRO HIRE ME NOW!', 'font-size: 50px; font-style: italic;');
	console.log('%c contact@haashemi.dev', 'font-style: italic;');
	console.log('%c https://github.com/haashemi', 'font-style: italic;');
	console.log('%c ----------------', 'font-size: 30px;');
</script>

<svelte:head>
	<title>Ali Hashemi</title>
	<meta name="description" content="Ali Hashemi's portfolio website." />
</svelte:head>

<main class="container mx-auto flex flex-col gap-4 p-3">
	<Header />

	<slot />
</main>
