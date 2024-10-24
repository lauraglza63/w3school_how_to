<script lang="ts">
	export let value: string;
	export let selected: string;
</script>

<button
	class="block w-full cursor-pointer border-none px-5 py-4 text-left text-black outline-none transition [transition:0.3s] hover:bg-[#ddd]"
	class:bg-[#ddd]={value === selected}
	on:click={() => (selected = value)}
>
	{value}
</button>
