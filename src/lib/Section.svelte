<script lang="ts">
	export let title: string;
	export let href: string;
</script>

<div class="space-y-5 rounded-xl border-2 border-slate-700/40 p-5">
	<div class="flex items-center justify-between">
		<h3 class="text-lg font-semibold italic">{title}</h3>
		<a {href} class="text-sm text-slate-300">View More</a>
	</div>

	<slot />
</div>
