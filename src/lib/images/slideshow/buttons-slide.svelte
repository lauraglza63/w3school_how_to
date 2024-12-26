<script lang="ts">
	export let direction: 'prev' | 'next' = 'prev';
</script>

<button
	class="whit absolute top-1/2 -mt-6 w-auto cursor-pointer select-none p-4 text-lg font-bold text-white duration-75 [transition:ease] hover:bg-black/80"
	class:rounded-br-md={direction === 'prev'}
	class:rounded-tr-md={direction === 'prev'}
	class:rounded-tl-md={direction === 'next'}
	class:rounded-bl-md={direction === 'next'}
	class:right-0={direction === 'next'}
	on:click
>
	<slot></slot>
</button>
