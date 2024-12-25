<script lang="ts">
	import { page } from '$app/stores';

	export let icon;
	export let href: string;
</script>

<a
	{href}
	data-active={$page.url.href.includes(href)}
	class="flex items-center gap-x-4 p-3 text-center text-lg text-white no-underline hover:bg-black data-[active=true]:bg-[#04aa6d] hover:data-[active=true]:bg-black sm:float-left sm:gap-x-2"
>
	<svelte:component this={icon}></svelte:component>
	<slot></slot>
</a>
