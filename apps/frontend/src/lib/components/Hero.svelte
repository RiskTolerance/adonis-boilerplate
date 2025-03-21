<script lang="ts">
	interface HeroContent {
		title: string;
		subtitle: string;
		image: string;
	}
	let { content: HeroContent } = $props();
</script>

<div class="bg-bDark text-bLight">
	<div class="container mx-auto p-4">
		<h1 class="text-4xl font-bold">{HeroContent.title}</h1>
		<p class="text-lg">{HeroContent.subtitle}</p>
		<img src={HeroContent.image} alt={HeroContent.title} />
	</div>
</div>
