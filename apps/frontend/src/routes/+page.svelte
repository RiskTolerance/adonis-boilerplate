<script lang="ts">
	import { Button, Calendar, Toggle } from 'bits-ui';
	import { MoonStar, Sun } from '@lucide/svelte';
	let toggled = $state(true);
	$effect(() => {
		console.log('toggled', toggled);
		let theme = document.querySelector('[data-theme]');
		theme?.setAttribute('data-theme', toggled ? 'dark' : 'light');
	});
</script>

<div class="container mx-auto p-4">
	<Button.Root
		onclick={() => {
			toggled = !toggled;
		}}
		class="rounded-lg bg-amber-400 p-2 dark:bg-slate-800"
	>
		{#if toggled}
			<MoonStar class="stroke-amber-200"></MoonStar>
		{:else}
			<Sun class="stroke-slate-700"></Sun>
		{/if}
	</Button.Root>
</div>
