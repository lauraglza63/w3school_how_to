<script>
	import Minus from 'lucide-svelte/icons/minus';
	import Plus from 'lucide-svelte/icons/plus';
	import { slide } from 'svelte/transition';

	let active = false;
</script>

<button
	class=" flex w-full cursor-pointer justify-between border-none bg-[#eee] p-[18px] text-left text-[#444] outline-none [transition:0.4s] hover:bg-[#ccc]"
	class:bg-[#ccc]={active}
	on:click={() => (active = !active)}
>
	<slot name="title" />
	<span class="text-2xl">
		{#if active}
			<Minus class="size-5" />
		{:else}
			<Plus class="size-5" />
		{/if}
	</span>
</button>
{#if active}
	<div class="panel block overflow-hidden bg-white px-[18px] py-2" transition:slide>
		<p>
			<slot />
		</p>
	</div>
{/if}
