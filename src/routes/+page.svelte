<script lang="ts">
	import { fade, fly } from 'svelte/transition';
	import Header from '$lib/Header.svelte';

	let isNavbarOpen = true;
</script>

{#if isNavbarOpen}
	<navbar
		transition:fade={{ duration: 200 }}
		class="fixed left-0 top-0 z-50 flex h-screen w-screen flex-col gap-4 bg-black/40 p-3 backdrop-blur-lg md:hidden"
	>
		<Header onClick={() => (isNavbarOpen = false)} ButtonIcon="X" />

		<div class="flex w-full grow justify-center px-3">
			<ul class="flex w-full flex-col gap-3 text-lg font-semibold">
				<a in:fade={{ duration: 300, delay: 100 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2"> Home </a>
				<a in:fade={{ duration: 300, delay: 150 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2">
					Projects
				</a>
				<a in:fade={{ duration: 300, delay: 200 }} href="/" class="w-full rounded-md border border-slate-800 bg-white/10 px-7 py-2"> Contact </a>
			</ul>
		</div>
	</navbar>
{/if}

<Header onClick={() => (isNavbarOpen = true)} ButtonIcon="=" />

<div class="relative space-y-2 rounded-xl border-2 border-slate-700/40 bg-black/25 px-6 py-10 backdrop-blur-lg">
	<h2 class="text-lg font-semibold italic">Junior Back-end Developer</h2>
	<p class="pl-2">
		Junior back-end developer with 3+ years of experience, including 1+ years of professional experience using Golang. Proficient in developing
		and maintaining high-performance, stable, and reliable web applications. Also interested in front-end development using modern web frameworks
		like React.
	</p>

	<div class="absolute bottom-0 right-0 -z-10 h-16 w-1/4 bg-slate-700 blur-3xl"></div>
</div>

<div class="flex flex-col md:flex-row">
	<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
		<h3 class="text-lg font-semibold italic">Projects</h3>

		<div class="flex items-center justify-around gap-4">
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-slate-500 shadow-lg shadow-slate-600 transition-all ease-in-out hover:-translate-y-1 hover:shadow-slate-700 motion-reduce:transition-none md:h-24 md:w-24"
				>X</a
			>
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-slate-500 p-3 shadow-lg shadow-slate-600 transition-all ease-in-out hover:-translate-y-1 hover:shadow-slate-700 motion-reduce:transition-none md:h-24 md:w-24"
			>
				<img src="/projects/zainox.png" alt="Zainox" />
			</a>
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-slate-500 shadow-lg shadow-slate-600 transition-all ease-in-out hover:-translate-y-1 hover:shadow-slate-700 motion-reduce:transition-none md:h-24 md:w-24"
				>X</a
			>
		</div>

		<div class="flex items-center justify-around gap-4">
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-slate-500 shadow-lg shadow-slate-600 transition-all ease-in-out hover:-translate-y-1 hover:shadow-slate-700 motion-reduce:transition-none md:h-24 md:w-24"
				>X</a
			>
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-slate-500 shadow-lg shadow-slate-600 transition-all ease-in-out hover:-translate-y-1 hover:shadow-slate-700 motion-reduce:transition-none md:h-24 md:w-24"
				>X</a
			>
			<a href="/" class="flex aspect-square h-20 w-20 items-center justify-center text-sm md:h-24 md:w-24">View More</a>
		</div>
	</div>

	<div></div>
</div>
