<script lang="ts">
	import TabContent from '$lib/menus/tab-headers/tab-content.svelte';
	import TabLink from '$lib/menus/tab-headers/tab-link.svelte';

	let selected = 'London';
</script>

<div>
	{#if selected === 'London'}
		<TabContent color="red">
			<h1 class="mb-4 text-5xl font-semibold">London</h1>
			<p class="text-xl">London is the capital city of England.</p>
		</TabContent>
	{:else if selected === 'Paris'}
		<TabContent color="green">
			<h1 class="mb-4 text-5xl font-semibold">Paris</h1>
			<p class="text-xl">Paris is the capital of France.</p>
		</TabContent>
	{:else if selected === 'Tokyo'}
		<TabContent color="blue">
			<h1 class="mb-4 text-5xl font-semibold">Tokyo</h1>
			<p class="text-xl">Tokyo is the capital of Japan.</p>
		</TabContent>
	{:else if selected === 'Oslo'}
		<TabContent color="orange">
			<h1 class="mb-4 text-5xl font-semibold">Oslo</h1>
			<p class="text-xl">Oslo is the capital of Norway.</p>
		</TabContent>
	{/if}
</div>

<div>
	<TabLink value="London" color="red" bind:selected>London</TabLink>
	<TabLink value="Paris" color="green" bind:selected>Paris</TabLink>
	<TabLink value="Tokyo" color="blue" bind:selected>Tokyo</TabLink>
	<TabLink value="Oslo" color="orange" bind:selected>Oslo</TabLink>
</div>
