<script lang="ts">
	//@ts-ignore
	import Icon from 'svelte-icons-pack/Icon.svelte';
	import GitHub from 'svelte-icons-pack/si/SiGithub';
	import MailDotRu from 'svelte-icons-pack/si/SiMaildotru';
	import Telegram from 'svelte-icons-pack/si/SiTelegram';
	import type { PageData } from './$types';

	export let data: PageData;
</script>

<svelte:head>
	<title>Ali Hashemi</title>
	<meta name="description" content="Ali Hashemi's portfolio website." />
</svelte:head>

<div class="py-20 text-center text-3xl font-medium">Junior Golang Developer</div>

<div class="container mx-auto p-3">
	<div class="grid gap-4 md:grid-cols-2 md:grid-rows-2">
		<div class="row-span-1 space-y-4 rounded-xl border-2 border-slate-700/40 bg-black/25 p-6 backdrop-blur-lg">
			<div class="flex items-center justify-between">
				<h3 class="text-lg font-semibold italic">Hi there!</h3>
			</div>

			<p class="pl-2 indent-4">
				I'm Ali Hashemi. A Junior back-end developer with <strong>3+ years</strong> of experience, including 1+ years of professional experience using
				Golang. Proficient in developing and maintaining high-performance, stable, and reliable web applications. Also interested in front-end development
				using modern web frameworks like Svelte and React.
			</p>
		</div>

		<div class="row-span-2 space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
			<div class="flex items-center justify-between">
				<h3 class="text-lg font-semibold italic">Skills</h3>
			</div>

			<div class="flex flex-wrap gap-3">
				{#each data.skills as skill}
					<p class="select-none rounded-full bg-white/20 px-3 py-1 font-medium transition-all hover:-translate-y-1 {skill.style}">
						{skill.name}
					</p>
				{/each}
			</div>
		</div>

		<div class="row-span-1 flex flex-col gap-5 rounded-xl border-2 border-slate-700/40 p-5">
			<div class="flex items-center justify-between">
				<h3 class="text-lg font-semibold italic">Get in touch!</h3>
			</div>

			<div class="flex grow flex-col justify-around gap-3">
				<a class="group relative z-10 overflow-hidden rounded-3xl border border-zinc-900 p-5" href="mailto:contact@haashemi.dev">
					<div class="flex items-center gap-3 font-mono text-base md:text-xl">
						<Icon src={MailDotRu} size="28" color="white" />
						<p class="whitespace-nowrap">contact@haashemi.dev</p>
					</div>
					<div
						id="mail-background"
						class="absolute right-0 h-full w-3/5 rounded-full bg-violet-500/40 blur-3xl transition-all duration-500 ease-in-out group-hover:right-1/2"
					/>
				</a>

				<a class="group relative z-10 overflow-hidden rounded-3xl border border-zinc-900 p-5" href="https://t.me/Byfron">
					<div class="flex items-center gap-3 font-mono text-base md:text-xl">
						<Icon src={Telegram} size="28" color="white" />
						<p class="whitespace-nowrap">@Byfron</p>
					</div>
					<div
						id="telegram-background"
						class="absolute left-0 h-full w-3/5 rounded-full bg-blue-500/40 blur-3xl transition-all duration-500 ease-in-out group-hover:left-[50%]"
					/>
				</a>

				<a class="group relative z-10 overflow-hidden rounded-3xl border border-zinc-900 p-5" href="https://github.com/haashemi">
					<div class="flex items-center gap-3 font-mono text-base md:text-xl">
						<Icon src={GitHub} size="28" color="white" />
						<p class="whitespace-nowrap">@haashemi</p>
					</div>
					<div
						id="github-background"
						class="absolute right-0 h-full w-3/5 rounded-full bg-zinc-500/40 blur-3xl transition-all duration-500 ease-in-out group-hover:right-1/2"
					/>
				</a>
			</div>
		</div>
	</div>
</div>
