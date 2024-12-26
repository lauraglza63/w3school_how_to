<script>
	export let value = 0;
	export let selected = 0;
</script>

<button
	data-active={selected === value}
	on:click={() => (selected = value)}
	class="dot mx-0 my-[2px] inline-block h-4 w-4 cursor-pointer rounded-full bg-[#bbb] transition-colors duration-75 [transition:ease] hover:bg-[#717171] data-[active=true]:bg-[#717171]"
></button>
