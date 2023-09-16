<script lang="ts">
	import Header from '$lib/Header.svelte';
	import Navbar from '$lib/Navbar.svelte';

	const skills = [
		{ name: 'Golang', style: 'hover:shadow-[0_0_30px_3px_#00ADD8d9] hover:bg-[#00ADD8]' },
		{ name: 'JS/TS', style: 'hover:text-black hover:shadow-[0_0_30px_3px_#F7DF1Ed9] hover:bg-[#F7DF1E]' },
		{ name: 'PostgreSQL', style: 'hover:shadow-[0_0_30px_3px_#4169E1d9] hover:bg-[#4169E1]' },
		{ name: 'SQLite', style: 'hover:shadow-[0_0_30px_3px_#003B57d9] hover:bg-[#003B57]' },
		{ name: 'Badger', style: 'hover:shadow-[0_0_30px_3px_#E50695d9] hover:bg-[#E50695]' },
		{ name: 'Redis', style: 'hover:shadow-[0_0_30px_3px_#DC382Dd9] hover:bg-[#DC382D]' },
		{ name: 'Next.JS', style: 'hover:shadow-[0_0_30px_3px_#000000d9] hover:bg-[#000000]' },
		{ name: 'React', style: 'hover:text-black hover:shadow-[0_0_30px_3px_#61DAFBd9] hover:bg-[#61DAFB]' },
		{ name: 'Svelte', style: 'hover:shadow-[0_0_30px_3px_#FF3E00d9] hover:bg-[#FF3E00]' },
		{ name: 'TailwindCSS', style: 'hover:shadow-[0_0_30px_3px_#06B6D4d9] hover:bg-[#06B6D4]' },
		{ name: 'Git', style: 'hover:shadow-[0_0_30px_3px_#F05032d9] hover:bg-[#F05032]' },
		{ name: 'Docker', style: 'hover:shadow-[0_0_30px_3px_#2496EDd9] hover:bg-[#2496ED]' },
		{ name: 'OpenTelemetry', style: 'hover:shadow-[0_0_30px_3px_#000000d9] hover:bg-[#000000]' },
		{ name: 'Nginx', style: 'hover:shadow-[0_0_30px_3px_#009639d9] hover:bg-[#009639]' },
	];

	let isNavbarOpen = false;
</script>

{#if isNavbarOpen}
	<Navbar onClick={() => (isNavbarOpen = false)} />
{/if}

<Header onClick={() => (isNavbarOpen = true)} ButtonIcon="=" />

<div class="relative space-y-4 rounded-xl border-2 border-slate-700/40 bg-black/25 p-6 backdrop-blur-lg">
	<h2 class="text-xl font-semibold italic">Junior Back-end Developer</h2>
	<p class="pl-2 indent-4">
		Junior back-end developer with 3+ years of experience, including 1+ years of professional experience using Golang. Proficient in developing
		and maintaining high-performance, stable, and reliable web applications. Also interested in front-end development using modern web frameworks
		like React and Svelte.
	</p>

	<div class="absolute bottom-0 right-0 -z-10 h-16 w-1/4 bg-slate-700 blur-3xl"></div>
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
			{#each skills as skill}
				<p class="select-none rounded-full bg-white/20 px-3 py-1 font-medium transition-all hover:-translate-y-1 {skill.style}">
					{skill.name}
				</p>
			{/each}
		</div>
	</div>
</div>
