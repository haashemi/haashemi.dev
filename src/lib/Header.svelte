<script lang="ts">
	import { afterNavigate } from '$app/navigation';
	import { fade } from 'svelte/transition';

	let isOpen = false;
	let routes = [
		{ title: 'Home', href: '/' },
		{ title: 'Projects', href: '/projects' },
		{ title: 'Skills', href: '/skills' },
		{ title: 'Contact', href: '/contact' },
	];

	afterNavigate(() => (isOpen = false));
</script>

<header class="sticky top-3 z-50 w-full">
	<div class="flex h-14 items-center justify-between overflow-hidden rounded-xl border-2 border-slate-700/40 bg-black/25 px-5 backdrop-blur-md">
		<h1 class="select-none text-xl font-bold">Ali Hashemi</h1>

		<div class="hidden gap-3 text-lg font-semibold md:flex">
			{#each routes as route}
				<a href={route.href}>{route.title}</a>
			{/each}
		</div>

		<button class="md:hidden" on:click={() => (isOpen = !isOpen)}>{isOpen ? 'X' : '='}</button>
	</div>
</header>

{#if isOpen}
	<navbar
		transition:fade={{ duration: 200 }}
		class="fixed left-0 top-0 z-40 flex h-screen w-screen flex-col gap-4 bg-black/40 pt-24 backdrop-blur-md md:hidden"
	>
		<ul class="flex w-full flex-col gap-3 px-5 text-lg font-semibold">
			{#each routes as route}
				<a in:fade={{ duration: 300, delay: 200 }} href={route.href} class="w-full rounded-md border border-slate-800 bg-white/10 px-5 py-2">
					{route.title}
				</a>
			{/each}
		</ul>

		<div aria-hidden="true" on:click={() => (isOpen = false)} class="grow"></div>
	</navbar>
{/if}
