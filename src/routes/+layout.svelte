<script>
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

<main class="min-h-screen w-full bg-black font-sans">
	<slot />
</main>
