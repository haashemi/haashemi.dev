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

<div class="grid gap-4 md:grid-cols-2 xl:grid-cols-3">
	<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
		<div class="flex items-center justify-between">
			<h3 class="text-lg font-semibold italic">Projects</h3>
			<a href="/" class="text-sm text-slate-300">View More</a>
		</div>

		<div class="flex flex-col gap-4">
			<a href="/" class="group relative flex h-20 gap-5 rounded-xl bg-stone-600/20">
				<div class="w-20 rounded-xl bg-gradient-to-br from-red-600 to-red-700 p-3">
					<img src="/projects/epic-center.png" alt="Epic-Center" />
				</div>

				<div class="flex flex-col justify-around whitespace-nowrap py-1 pr-5 font-sans">
					<h2 class="text-lg font-semibold italic">Epic Center</h2>
					<h3 class="text-xs">FullStack Developer</h3>
					<p class="text-xs text-zinc-500">Aug 2022 - Present</p>
				</div>

				<div class="absolute -z-10 h-20 w-20 rounded-xl bg-red-900 blur-md transition-all group-hover:bg-red-800 group-hover:blur-lg" />
			</a>

			<a href="/" class="group relative flex h-20 gap-5 rounded-xl bg-white/5">
				<div class="w-20 rounded-xl bg-gradient-to-br from-blue-600 to-blue-700 p-3">
					<img src="/projects/zainox.png" alt="Zainox" />
				</div>

				<div class="flex flex-col justify-around whitespace-nowrap py-1 pr-5 font-sans">
					<h2 class="text-lg font-semibold italic">Zainox</h2>
					<h3 class="text-xs">Back-End Developer</h3>
					<p class="text-xs text-zinc-500">Aug 2022 - Present</p>
				</div>

				<div class="absolute -z-10 h-20 w-20 rounded-xl bg-blue-900 blur-md transition-all group-hover:bg-blue-800 group-hover:blur-lg" />
			</a>

			<a href="/" class="group relative flex h-20 gap-5 rounded-xl bg-white/5">
				<div class="w-20 rounded-xl bg-gradient-to-br from-violet-600 to-violet-700 p-3">
					<img src="/projects/llamanite.png" alt="LlamaNite" />
				</div>

				<div class="flex flex-col justify-around whitespace-nowrap py-1 pr-5 font-sans">
					<h2 class="text-lg font-semibold italic">LlamaNite</h2>
					<h3 class="text-xs">Back-End Developer</h3>
					<p class="text-xs text-zinc-500">Jan 2021 - Aug 2022</p>
				</div>

				<div class="absolute -z-30 h-20 w-20 rounded-xl bg-violet-900 blur-md transition-all group-hover:bg-violet-800 group-hover:blur-lg" />
			</a>
		</div>
	</div>

	<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5 xl:col-span-2">
		<div class="flex items-center justify-between">
			<h3 class="text-lg font-semibold italic">Skills</h3>
			<a href="/" class="text-sm text-slate-300">View More</a>
		</div>

		<div class="flex flex-wrap gap-3">
			{#each data.skills as skill}
				<p class="select-none rounded-full bg-white/20 px-3 py-1 font-medium transition-all hover:-translate-y-1 {skill.style}">
					{skill.name}
				</p>
			{/each}
		</div>
	</div>
</div>
