<script lang="ts">
	import { fade } from 'svelte/transition';

	let isOpen = false;
</script>

<header class="sticky top-0 z-50 w-full p-3">
	<div class="flex h-14 items-center justify-between overflow-hidden rounded-xl border-2 border-slate-700/40 bg-black/25 px-5 backdrop-blur-xl">
		<h1 class="relative text-xl font-bold">
			<div class="absolute -left-12 -top-1 -z-10 h-16 w-64 bg-slate-800 blur-3xl" />
			Ali Hashemi
		</h1>

		<div class="hidden gap-3 text-lg font-semibold md:flex">
			<a href="/">Home</a>
			<a href="/">Projects</a>
			<a href="/">Contact Me</a>
		</div>

		<button class="md:hidden" on:click={() => (isOpen = !isOpen)}>{isOpen ? 'X' : '='}</button>
	</div>
</header>

{#if isOpen}
	<navbar
		transition:fade={{ duration: 200 }}
		class="fixed left-0 top-0 z-40 flex h-screen w-screen flex-col gap-4 bg-black/40 pt-24 backdrop-blur-xl md:hidden"
	>
		<ul class="flex w-full flex-col gap-3 px-5 text-lg font-semibold">
			<a in:fade={{ duration: 300, delay: 200 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-5 py-2">Home</a>
			<a in:fade={{ duration: 300, delay: 300 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-5 py-2">Projects</a>
			<a in:fade={{ duration: 300, delay: 400 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-5 py-2">Contact</a>
		</ul>

		<div aria-hidden="true" on:click={() => (isOpen = false)} class="grow"></div>
	</navbar>
{/if}
