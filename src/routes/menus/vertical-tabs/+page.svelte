<script lang="ts">
	import TabContent from '$lib/menus/vertical-tabs/tab-content.svelte';
	import TabItem from '$lib/menus/vertical-tabs/tab-item.svelte';

	let selected = 'London';
</script>

<div class="box-border border">
	<div class="tab float-left h-screen w-[30%] border border-[#ccc] bg-[#f1f1f1]">
		<TabItem value="London" bind:selected />
		<TabItem value="Paris" bind:selected />
		<TabItem value="Tokyo" bind:selected />
	</div>

	<div>
		<TabContent value="London" bind:selected>
			<h3 class="text-2xl font-bold">London</h3>
			<p>London is the capital city of England.</p>
		</TabContent>
		<TabContent value="Paris" bind:selected>
			<h3 class="text-2xl font-bold">Paris</h3>
			<p>Paris is the capital of France.</p>
		</TabContent>
		<TabContent value="Tokyo" bind:selected>
			<h3 class="text-2xl font-bold">Tokyo</h3>
			<p>Tokyo is the capital of Japan.</p>
		</TabContent>
	</div>
</div>
