<script lang="ts">
	export let ButtonIcon = '=';
	export let onClick: () => void;
</script>

<header class="flex h-14 w-full items-center justify-between rounded-xl border-2 border-slate-700/40 bg-black/25 px-5 backdrop-blur-lg">
	<h1 class="relative text-xl font-bold">
		<div class="absolute -left-12 -top-1 -z-10 h-16 w-64 bg-slate-800 blur-3xl"></div>
		Ali Hashemi
	</h1>

	<div class="hidden gap-3 text-lg font-semibold md:flex">
		<a href="/">Home</a>
		<a href="/">Projects</a>
		<a href="/">Contact Me</a>
	</div>

	<button class="md:hidden" on:click={onClick}>{ButtonIcon}</button>
</header>
