<script lang="ts">
	import { afterNavigate } from '$app/navigation';
	//@ts-ignore
	import Icon from 'svelte-icons-pack/Icon.svelte';
	import CgClose from 'svelte-icons-pack/cg/CgClose';
	import CgMenuRight from 'svelte-icons-pack/cg/CgMenuRight';
	import { fade, fly } from 'svelte/transition';

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
	<div
		class="flex h-14 items-center justify-between overflow-hidden rounded-xl border-2 border-slate-700/40 bg-black/25 px-3 backdrop-blur-md sm:px-5"
	>
		<h1 class="select-none text-xl font-bold">Ali Hashemi</h1>

		<div class="hidden gap-7 text-lg font-semibold md:flex">
			{#each routes as route}
				<a class="transition-colors duration-200 hover:text-slate-400" href={route.href}>{route.title}</a>
			{/each}
		</div>

		<button class="relative h-12 w-12 md:hidden" on:click={() => (isOpen = !isOpen)}>
			{#if isOpen}
				<span transition:fade={{ duration: 150 }} class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2">
					<Icon src={CgClose} size="28" color="white" />
				</span>
			{:else}
				<span
					in:fly={{ duration: 250, x: -20 }}
					out:fly={{ duration: 250, x: 20 }}
					class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2"
				>
					<Icon src={CgMenuRight} size="28" color="white" />
				</span>
			{/if}
		</button>
	</div>
</header>

{#if isOpen}
	<navbar
		in:fade={{ duration: 200 }}
		out:fade={{ duration: 300, delay: 100 }}
		class="fixed left-0 top-0 z-40 flex h-screen w-screen flex-col gap-4 bg-black/40 pt-24 backdrop-blur-md md:hidden"
	>
		<ul class="flex w-full flex-col gap-3 px-5 text-lg font-semibold">
			{#each routes as route, i (route.title)}
				<a
					in:fly|global={{ duration: 300, delay: 150 + i * 50, x: -30 }}
					out:fly|global={{ duration: 300, delay: i * 50, x: 30 }}
					href={route.href}
					class="w-full rounded-md border border-slate-800 bg-white/10 px-5 py-2"
				>
					{route.title}
				</a>
			{/each}
		</ul>

		<div aria-hidden="true" on:click={() => (isOpen = false)} class="grow"></div>
	</navbar>
{/if}
