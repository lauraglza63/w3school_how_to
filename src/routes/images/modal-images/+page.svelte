<script lang="ts">
	let src = '/img/img_snow_wide.jpg';
	let alt = 'Snow';
	let open = false;
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<img
	class="[transition: 0.3s] m-5 w-full max-w-80 cursor-pointer rounded-md hover:opacity-70"
	on:click={() => (open = true)}
	{src}
	{alt}
/>

<!-- The Modal -->
<div
	data-open={open}
	class="modal fixed left-0 top-0 z-[1] h-full w-full overflow-auto bg-black bg-black/90 pt-[100px] data-[open=false]:hidden"
>
	<!-- The Close Button -->
	<button
		class="[transition: 0.3s] absolute right-9 top-4 text-4xl font-bold text-[#f1f1f1] hover:text-[#bbb] focus:text-[#bbb]"
		on:click={() => (open = false)}
	>
		&times;</button
	>

	<!-- Modal Content (The Image) -->
	<img class="animation-zoom m-auto block w-full max-w-[700px] rounded-md sm:w-[80%]" {src} {alt} />

	<!-- Modal Caption (Image Text) -->
	<div
		class="animation-zoom m-auto mt-5 block h-[150px] w-[80%] max-w-[700px] px-2 py-0 text-center text-[#ccc]"
	>
		{alt}
	</div>
</div>

<style>
	.animation-zoom {
		animation-name: zoom;
		animation-duration: 0.6s;
	}

	@keyframes zoom {
		from {
			transform: scale(0);
		}
		to {
			transform: scale(1);
		}
	}
</style>
