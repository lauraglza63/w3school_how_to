<script lang="ts">
	import TopnavLink from '$lib/menus/responsive-topnav/topnav-link.svelte';
	import { Menu } from 'lucide-svelte';
	export let openMenu = false;
</script>

<div class="topnav relative overflow-hidden bg-[#333]" id="myTopnav">
	<TopnavLink href="#home" responsive={openMenu}>Home</TopnavLink>
	<TopnavLink href="#news" responsive={openMenu}>News</TopnavLink>
	<TopnavLink href="#contact" responsive={openMenu}>Contact</TopnavLink>
	<TopnavLink href="#about" responsive={openMenu}>About</TopnavLink>
	<button
		class="icon absolute right-0 top-0 float-right block px-[14px] py-4 invert hover:bg-[#ddd] hover:invert-0 sm:hidden"
		on:click={() => (openMenu = !openMenu)}
	>
		<Menu class="size-7"></Menu>
	</button>
</div>
