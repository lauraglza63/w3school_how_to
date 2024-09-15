<script lang="ts">
	import HorizontalElement from '$lib/menus/icon-bar/horizontal-element..svelte';
	import VerticalElement from '$lib/menus/icon-bar/vertical-element.svelte';
	import Earth from 'lucide-svelte/icons/earth';
	import House from 'lucide-svelte/icons/house';
	import Mail from 'lucide-svelte/icons/mail';
	import Search from 'lucide-svelte/icons/search';
	import Trash_2 from 'lucide-svelte/icons/trash-2';

	let activeVertical = 'house';
	let activeHorizontal = 'house';
</script>

<div class="flex w-full p-4">
	<div class="p-2">
		<p class="text-lg">Vertical</p>
		<div class="w-24 bg-[#555]">
			<VerticalElement icon={House} bind:active={activeVertical} goto="house" />
			<VerticalElement icon={Search} bind:active={activeVertical} goto="search" />
			<VerticalElement icon={Mail} bind:active={activeVertical} goto="mail" />
			<VerticalElement icon={Earth} bind:active={activeVertical} goto="earth" />
			<VerticalElement icon={Trash_2} bind:active={activeVertical} goto="trash" />
		</div>
	</div>

	<div class="w-full p-2">
		<p class="text-lg">Horizontal</p>
		<div class="w-full overflow-auto bg-[#555]">
			<HorizontalElement icon={House} bind:active={activeHorizontal} goto="house" />
			<HorizontalElement icon={Search} bind:active={activeHorizontal} goto="search" />
			<HorizontalElement icon={Mail} bind:active={activeHorizontal} goto="mail" />
			<HorizontalElement icon={Earth} bind:active={activeHorizontal} goto="earth" />
			<HorizontalElement icon={Trash_2} bind:active={activeHorizontal} goto="trash" />
		</div>
	</div>
</div>
