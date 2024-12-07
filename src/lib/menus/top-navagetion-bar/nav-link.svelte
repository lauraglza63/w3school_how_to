<script lang="ts">
	import { page } from '$app/stores';

	export let href: string;
	$: pageHref = $page.url.href;
</script>

<a
	data-active={pageHref.includes(href)}
	class="float-left px-[14px] py-4 text-center text-lg text-[#f2f2f2] hover:bg-[#ddd] hover:text-black data-[active=true]:bg-[#04aa6d] data-[active=true]:text-white"
	{href}
>
	<slot />
</a>
