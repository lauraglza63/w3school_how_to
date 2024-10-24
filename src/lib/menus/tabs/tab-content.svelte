<script>
	import { fade } from 'svelte/transition';
</script>

<div class="border border-t-0 border-solid border-[#ccc] px-3 py-2" in:fade={{ duration: 800 }}>
	<slot />
</div>
