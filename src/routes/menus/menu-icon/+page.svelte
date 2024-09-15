<script lang="ts">
	let open = false;
</script>

<button class="m-10 inline-block cursor-pointer" on:click={() => (open = !open)}>
	<div
		class="bar1 my-[6px] h-[5px] w-[35px] bg-[#333] [transition:0.4s]"
		class:transform={open}
		class:translate-y-[11px]={open}
		class:-rotate-45={open}
	/>
	<div class="bar2 my-[6px] h-[5px] w-[35px] bg-[#333] [transition:0.4s]" class:opacity-0={open} />
	<div
		class="bar3 my-[6px] h-[5px] w-[35px] bg-[#333] [transition:0.4s]"
		class:transform={open}
		class:translate-y-[-11px]={open}
		class:rotate-45={open}
	/>
</button>
