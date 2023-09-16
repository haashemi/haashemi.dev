<script lang="ts">
	import { fade } from 'svelte/transition';
	import Header from '$lib/Header.svelte';

	export let onClick: () => void;
</script>

<navbar
	transition:fade={{ duration: 200 }}
	class="fixed left-0 top-0 z-50 flex h-screen w-screen flex-col gap-4 bg-black/40 p-3 backdrop-blur-lg md:hidden"
>
	<Header {onClick} ButtonIcon="X" />

	<div class="flex w-full grow justify-center px-3">
		<ul class="flex w-full flex-col gap-3 text-lg font-semibold">
			<a in:fade={{ duration: 300, delay: 100 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2"> Home </a>
			<a in:fade={{ duration: 300, delay: 150 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2"> Projects </a>
			<a in:fade={{ duration: 300, delay: 200 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2"> Contact </a>
		</ul>
	</div>
</navbar>
