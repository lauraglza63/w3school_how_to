<script lang="ts">
	export let value: string;
	export let selected: string;
	export let color: string = 'grey';
</script>

<button
	class="float-left w-1/4 cursor-pointer border-none bg-[#555] px-[14px] py-4 text-lg text-white outline-none hover:bg-[#777]"
	{...value === selected ? { style: `background-color: ${color}` } : {}}
	on:click={() => (selected = value)}
>
	<slot />
</button>
