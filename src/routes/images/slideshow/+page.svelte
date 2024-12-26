<script lang="ts">
	import Carousel from '$lib/images/slideshow/carousel.svelte';

	const images = ['/img/img_nature_wide.jpg', '/img/img_snow_wide.jpg', '/img/img_lights_wide.jpg'];
</script>

<div class="flex h-screen items-center justify-center">
	<Carousel {images} />
</div>
