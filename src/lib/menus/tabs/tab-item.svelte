<script lang="ts">
	export let value: string;
	export let selected: string;
</script>

<button
	class="[transition: 0.3s] float-left cursor-pointer border-none bg-inherit px-4 py-3 outline-none hover:bg-[#ddd]"
	class:bg-[#ddd]={selected === value}
	on:click={() => (selected = value)}
>
	{value}
</button>
