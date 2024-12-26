<script lang="ts">
	export let direction: 'prev' | 'next' = 'prev';
</script>

<button
	data-direction={direction}
	class="absolute top-[40%] -mt-12 w-auto cursor-pointer select-none p-4 text-xl font-bold text-white hover:bg-black/80 data-[direction=next]:right-0 data-[direction=next]:rounded-bl-md data-[direction=next]:rounded-tl-md data-[direction=prev]:rounded-br-md data-[direction=prev]:rounded-tr-md"
	style="-webkit-user-select: none;"
	on:click
>
	<slot></slot>
</button>
