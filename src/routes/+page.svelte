<script lang="ts">
	import type { PageData } from './$types';

	export let data: PageData;
</script>

<div class="relative space-y-4 rounded-xl border-2 border-slate-700/40 bg-black/25 p-6 backdrop-blur-lg">
	<h2 class="text-xl font-semibold italic">{data.info.title}</h2>
	<p class="pl-2 indent-4">{data.info.text}</p>

	<div class="absolute -left-12 top-0 -z-10 h-20 w-64 bg-slate-800 blur-3xl" />
	<div class="absolute bottom-0 right-0 -z-10 h-16 w-1/4 bg-slate-800 blur-3xl" />
</div>

<div class="flex flex-col gap-4 md:flex-row">
	<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
		<h3 class="text-lg font-semibold italic">Projects</h3>

		<div class="flex items-center justify-around gap-4">
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl bg-gradient-to-br
				from-red-600 to-orange-600 p-5 shadow-lg shadow-red-700
				transition-all ease-in-out hover:-translate-y-1 hover:shadow-red-800 motion-reduce:transition-none md:h-24 md:w-24"
			>
				<img src="/projects/epic-center.png" alt="Epic-Center" />
			</a>
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl
				bg-gradient-to-br from-blue-700 to-sky-600 p-5 shadow-lg shadow-blue-600
				transition-all ease-in-out hover:-translate-y-1 hover:shadow-blue-700 motion-reduce:transition-none md:h-24 md:w-24"
			>
				<img src="/projects/zainox.png" alt="Zainox" />
			</a>
			<a
				href="/"
				class="flex aspect-square h-20 w-20 items-center justify-center rounded-2xl
				bg-gradient-to-br from-purple-700 to-violet-600 p-5 shadow-lg shadow-violet-600
				transition-all ease-in-out hover:-translate-y-1 hover:shadow-violet-700 motion-reduce:transition-none md:h-24 md:w-24"
			>
				<img src="/projects/llamanite.png" alt="Zainox" />
			</a>
		</div>
	</div>

	<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
		<h3 class="text-lg font-semibold italic">Skills</h3>

		<div class="flex flex-wrap gap-3">
			{#each data.skills as skill}
				<p class="select-none rounded-full bg-white/20 px-3 py-1 font-medium transition-all hover:-translate-y-1 {skill.style}">
					{skill.name}
				</p>
			{/each}
		</div>
	</div>
</div>
