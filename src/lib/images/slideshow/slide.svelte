<script>
	import { fade } from 'svelte/transition';

	export let src = '';
	export let active = false;
</script>

<div
	class="relative"
	in:fade={{ duration: 600 }}
	class:opacity-100={active}
	class:opacity-0={!active}
>
	<div class="absolute top-0 px-2 py-3 text-xs text-[#f2f2f2]">
		<slot name="upper-text"></slot>
	</div>
	<img {src} alt="" class="w-full" />
	<div class="absolute bottom-2 w-full px-2 py-3 text-center text-base text-[#f2f2f2]">
		<slot name="under-text"></slot>
	</div>
</div>
