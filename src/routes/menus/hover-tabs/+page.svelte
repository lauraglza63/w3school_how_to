<script lang="ts">
	import Tabcontent from '$lib/menus/hover-tabs/tabcontent.svelte';
	import Tablink from '$lib/menus/hover-tabs/tablink.svelte';

	let activeTab = 'London';
</script>

<div class="tab float-left h-screen w-[30%] border border-[#ccc] bg-[#f1f1f1]">
	<Tablink bind:selected={activeTab} value="London" />
	<Tablink bind:selected={activeTab} value="Paris" />
	<Tablink bind:selected={activeTab} value="Tokyo" />
</div>

{#if activeTab === 'London'}
	<Tabcontent>
		<h3 class="mb-2 text-4xl font-semibold">London</h3>
		<p>London is the capital city of England.</p>
	</Tabcontent>
{:else if activeTab === 'Paris'}
	<Tabcontent>
		<h3 class="mb-2 text-4xl font-semibold">Paris</h3>
		<p>Paris is the capital of France.</p>
	</Tabcontent>
{:else if activeTab === 'Tokyo'}
	<Tabcontent>
		<h3 class="mb-2 text-4xl font-semibold">Tokyo</h3>
		<p>Tokyo is the capital of Japan.</p>
	</Tabcontent>
{/if}
