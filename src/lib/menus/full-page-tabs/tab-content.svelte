<script>
	export let color = '';
</script>

<div class="h-full px-[100px] pt-52 text-white" style="background-color: {color};">
	<h3 class="text-3xl">
		<slot name="title" />
	</h3>
	<p class="text-lg">
		<slot />
	</p>
</div>
