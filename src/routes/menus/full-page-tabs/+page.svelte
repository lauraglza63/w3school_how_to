<script lang="ts">
	import TabContent from '$lib/menus/full-page-tabs/tab-content.svelte';
	import Tablink from '$lib/menus/full-page-tabs/tab-link.svelte';
	let selected = 'Home';
</script>

<div class="m-0 h-screen">
	<div>
		<Tablink value="Home" bind:selected color="red">Home</Tablink>
		<Tablink value="News" bind:selected color="green">News</Tablink>
		<Tablink value="Contact" bind:selected color="blue">Contact</Tablink>
		<Tablink value="About" bind:selected color="orange">About</Tablink>
	</div>

	{#if selected === 'Home'}
		<TabContent color="red">
			<svelte:fragment slot="title">Home</svelte:fragment>
			<svelte:fragment>Home is where the heart is..</svelte:fragment>
		</TabContent>
	{:else if selected === 'News'}
		<TabContent color="green">
			<svelte:fragment slot="title">News</svelte:fragment>
			<svelte:fragment>Some news this fine day!</svelte:fragment>
		</TabContent>
	{:else if selected === 'Contact'}
		<TabContent color="blue">
			<svelte:fragment slot="title">Contact</svelte:fragment>
			<svelte:fragment>Get in touch, or swing by for a cup of coffee.</svelte:fragment>
		</TabContent>
	{:else if selected === 'About'}
		<TabContent color="orange">
			<svelte:fragment slot="title">About</svelte:fragment>
			<svelte:fragment>Who we are and what we do.</svelte:fragment>
		</TabContent>
	{/if}
</div>
