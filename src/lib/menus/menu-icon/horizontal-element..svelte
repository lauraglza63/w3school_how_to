<script lang="ts">
	import type { Icon } from 'lucide-svelte';
	import type { ComponentType } from 'svelte';

	export let icon: ComponentType<Icon>;
	export let active: string;
	export let goto: string;
</script>

<a
	href=" "
	class="float-left w-[20%] py-3 transition-all hover:bg-[#000]"
	class:bg-[#04AA6D]={active === goto}
	on:click={() => (active = goto)}
>
	<svelte:component this={icon} class="m-auto size-9 text-center text-white" />
</a>
