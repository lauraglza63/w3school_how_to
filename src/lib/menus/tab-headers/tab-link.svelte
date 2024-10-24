<script lang="ts">
	export let value: string;
	export let selected: string;
	export let color: string = '#555';
</script>

<button
	class="float-left h-16 w-1/4 cursor-pointer border-none bg-[#555] px-3 py-4 text-lg text-white outline-none hover:bg-[#777]"
	on:click={() => (selected = value)}
	{...value === selected ? { style: `background-color: ${color}` } : {}}
>
	<slot />
</button>
