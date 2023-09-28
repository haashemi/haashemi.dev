<script lang="ts">
	//@ts-ignore
	import Icon from 'svelte-icons-pack/Icon.svelte';
	import GitHub from 'svelte-icons-pack/si/SiGitHub.js';
	import MailDotRu from 'svelte-icons-pack/si/SiMaildotru.js';
	import Telegram from 'svelte-icons-pack/si/SiTelegram.js';
</script>

<h1 class="my-10 text-center text-4xl font-semibold">Get in touch!</h1>

<div class="grid gap-5 md:grid-cols-2 lg:grid-cols-3">
	<a href="mailto:contact@haashemi.dev" class="group relative overflow-hidden rounded-3xl border border-zinc-900 p-5">
		<h2 class="font-semibold italic">Want to have a professional talk?</h2>

		<div
			class="flex h-40 items-center justify-center gap-3 font-mono text-xl transition-transform duration-300 ease-in-out group-hover:scale-110"
		>
			<Icon src={MailDotRu} size="28" color="white" />
			<p class="whitespace-nowrap">contact@haashemi.dev</p>
		</div>

		<div
			class="absolute -bottom-1/2 -left-1/3 h-full w-full rounded-full bg-violet-500/20 blur-3xl transition-transform duration-300 ease-in-out group-hover:scale-150"
		/>
	</a>

	<a href="https://t.me/Byfron" class="group relative overflow-hidden rounded-3xl border border-zinc-900 p-5">
		<h2 class="font-semibold italic">Want to say Hi?</h2>

		<div
			class="flex h-40 items-center justify-center gap-3 font-mono text-xl transition-transform duration-300 ease-in-out group-hover:scale-110"
		>
			<Icon src={Telegram} size="28" color="white" />
			<p class="whitespace-nowrap">@Byfron</p>
		</div>

		<div
			class="absolute -bottom-1/2 -left-1/3 h-full w-full rounded-full bg-blue-500/20 blur-3xl transition-transform duration-300 ease-in-out group-hover:scale-150"
		/>
	</a>

	<a href="https://github.com/haashemi" class="group relative overflow-hidden rounded-3xl border border-zinc-900 p-5">
		<h2 class="font-semibold italic">Want to see my activity?</h2>

		<div
			class="flex h-40 items-center justify-center gap-3 font-mono text-xl transition-transform duration-300 ease-in-out group-hover:scale-110"
		>
			<Icon src={GitHub} size="28" color="white" />
			<p class="whitespace-nowrap">@haashemi</p>
		</div>

		<div
			class="absolute -bottom-1/2 -left-1/3 h-full w-full rounded-full bg-zinc-500/20 blur-3xl transition-transform duration-300 ease-in-out group-hover:scale-150"
		/>
	</a>
</div>
