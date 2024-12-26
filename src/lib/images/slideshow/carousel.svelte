<script lang="ts">
	import ButtonsSlide from '$lib/images/slideshow/buttons-slide.svelte';
	import Dot from '$lib/images/slideshow/dot.svelte';
	import Slide from '$lib/images/slideshow/slide.svelte';

	export let images: string[];
	let activeSlide = 0;
</script>

<div>
	<div class="slideshow-container relative m-auto max-w-[1000px]">
		{#each images as image, index}
			{#if index === activeSlide}
				<Slide src={image} active={true}>
					<svelte:fragment slot="upper-text">{index + 1} / {images.length}</svelte:fragment>
					<svelte:fragment slot="under-text">Caption {index + 1}</svelte:fragment>
				</Slide>
			{/if}
		{/each}

		<ButtonsSlide on:click={() => (activeSlide = (activeSlide - 1 + images.length) % images.length)}
			>&#10094;</ButtonsSlide
		>
		<ButtonsSlide
			on:click={() => (activeSlide = (activeSlide + 1) % images.length)}
			direction="next">&#10095;</ButtonsSlide
		>
	</div>
	<br />

	<div class="space-x-1 text-center">
		{#each images as _, index}
			<Dot bind:selected={activeSlide} value={index} />
		{/each}
	</div>
</div>
