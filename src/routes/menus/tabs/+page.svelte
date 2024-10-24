<script>
	import TabContent from '$lib/menus/tabs/tab-content.svelte';
	import TabItem from '$lib/menus/tabs/tab-item.svelte';
	let selected = 'London';
</script>

<!-- Tab links -->
<div class="overflow-hidden border border-solid border-[#ccc] bg-[#f1f1f1]">
	<TabItem value="London" bind:selected />
	<TabItem value="Paris" bind:selected />
	<TabItem value="Tokyo" bind:selected />
</div>
<!-- Tab contents -->
{#if selected === 'London'}
	<TabContent>
		<h3>London</h3>
		<p>London is the capital city of England.</p>
	</TabContent>
{:else if selected === 'Paris'}
	<TabContent>
		<h3>Paris</h3>
		<p>Paris is the capital of France.</p>
	</TabContent>
{:else if selected === 'Tokyo'}
	<TabContent>
		<h3>Tokyo</h3>
		<p>Tokyo is the capital of Japan.</p>
	</TabContent>
{/if}
