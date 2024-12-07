<script lang="ts">
	export let selected: string;
	export let value: string;
</script>

<button
	data-active={selected === value}
	class="block w-full cursor-pointer border-none bg-inherit px-[22px] py-4 text-left capitalize text-black outline-none hover:bg-[#ddd] data-[active=true]:bg-[#ccc]"
	on:mouseenter={() => (selected = value)}
>
	{value}
</button>
