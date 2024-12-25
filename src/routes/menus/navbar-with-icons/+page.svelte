<script>
	import NavbarLink from '$lib/menus/navbar-with-icons/navbar-link.svelte';
	import House from 'lucide-svelte/icons/house';
	import Mail from 'lucide-svelte/icons/mail';
	import Search from 'lucide-svelte/icons/search';
	import User from 'lucide-svelte/icons/user';
</script>

<div class="navbar w-full overflow-auto bg-[#555]">
	<NavbarLink href="#home" icon={House}>Home</NavbarLink>
	<NavbarLink href="#search" icon={Search}>Search</NavbarLink>
	<NavbarLink href="#about" icon={Mail}>Contact</NavbarLink>
	<NavbarLink href="#login" icon={User}>Login</NavbarLink>
</div>
