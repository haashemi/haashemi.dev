<script lang="ts">
	import Section from '$lib/Section.svelte';
	import type { PageData } from './$types';

	export let data: PageData;
</script>

<!-- About Me Section -->
<div class="relative space-y-4 rounded-xl border-2 border-slate-700/40 bg-black/25 p-6 backdrop-blur-lg">
	<h2 class="text-xl font-semibold italic">{data.info.title}</h2>
	<p class="pl-2 indent-4">{data.info.text}</p>

	<div class="absolute -left-12 top-0 -z-10 h-20 w-64 bg-slate-800 blur-3xl" />
	<div class="absolute bottom-0 right-0 -z-10 h-16 w-1/4 bg-slate-800 blur-3xl" />
</div>

<div class="grid gap-4 md:grid-cols-2 xl:grid-cols-3">
	<Section title="Projects" href="/projects">
		<div class="flex flex-col gap-4">
			{#each data.projects as p}
				<a href={p.url} class="flex h-20 gap-5 rounded-xl bg-zinc-900/50">
					<div class="aspect-square h-20 w-20 rounded-xl bg-gradient-to-br from-slate-800 to-slate-700 p-3">
						<img src={p.image} alt={p.title} />
					</div>

					<div class="flex flex-col justify-around whitespace-nowrap py-3 font-sans">
						<h2 class="text-lg font-semibold">{p.title}</h2>
						<p class="text-xs text-zinc-500">{p.duration}</p>
					</div>

					<div></div>
				</a>
			{/each}
		</div>
	</Section>

	<Section title="Skills" href="/skills">
		<div class="flex flex-wrap gap-3">
			{#each data.skills as skill}
				<p class="select-none rounded-full bg-white/20 px-3 py-1 font-medium transition-all hover:-translate-y-1 {skill.style}">
					{skill.name}
				</p>
			{/each}
		</div>
	</Section>

	<Section title="Social Media" href="/contact">
		<div class="flex flex-col justify-around gap-3 whitespace-nowrap text-lg italic text-zinc-500">
			{#each data.socialMedia as sm}
				<a href={sm.href}>{sm.name}: <span class="font-mono not-italic text-white">{sm.username}</span></a>
			{/each}
		</div>
	</Section>
</div>
