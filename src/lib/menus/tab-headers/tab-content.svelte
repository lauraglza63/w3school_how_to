<script lang="ts">
	export let color: string = 'black';
</script>

<div
	class="tabcontent h-[calc(100vh-64px)] p-12 text-center text-white"
	style="background-color: {color};"
>
	<slot />
</div>
