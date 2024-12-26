<script lang="ts">
	import ButtonSlide from '$lib/images/slideshow-galery/button-slide.svelte';

	let slideIndex = 0;
	const images = [
		{
			src: '/img/img_woods_wide.jpg',
			alt: 'The Woods'
		},
		{
			src: '/img/img_5terre_wide.jpg',
			alt: 'Cinque Terre'
		},
		{
			src: '/img/img_mountains_wide.jpg',
			alt: 'Mountains and fjords'
		},
		{
			src: '/img/img_lights_wide.jpg',
			alt: 'Northern Lights'
		},
		{
			src: '/img/img_nature_wide.jpg',
			alt: 'Nature and sunrise'
		},
		{
			src: '/img/img_snow_wide.jpg',
			alt: 'Snowy Mountains'
		}
	];
</script>

<div>
	<div class="relative">
		{#each images as image, index}
			{#if index === slideIndex}
				<div>
					<div class="numbertext absolute top-0 px-2 py-3 text-xs text-[#f2f2f2]">
						{index + 1} / {images.length}
					</div>
					<img src={image.src} class="w-full" alt={image.alt} />
				</div>
			{/if}
		{/each}

		<ButtonSlide on:click={() => (slideIndex = (slideIndex - 1 + images.length) % images.length)}
			>&#10094;</ButtonSlide
		>
		<ButtonSlide on:click={() => (slideIndex = (slideIndex + 1) % images.length)} direction="next"
			>&#10095;</ButtonSlide
		>

		<div class="caption-container bg-[#222] px-[2px] py-3 text-center text-white">
			<p>{images[slideIndex].alt}</p>
		</div>

		<div
			class="row clear-both grid"
			style="grid-template-columns: repeat({images.length}, minmax(0, 1fr));"
		>
			{#each images as image, index}
				<!-- content here -->
				<div class="float-left">
					<!-- svelte-ignore a11y-click-events-have-key-events -->
					<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
					<img
						data-active={slideIndex === index}
						class="w-full cursor-pointer opacity-60 hover:opacity-100 data-[active=true]:opacity-100"
						src={image.src}
						alt={image.alt}
						on:click={() => (slideIndex = index)}
					/>
				</div>
			{/each}
		</div>
	</div>
</div>
