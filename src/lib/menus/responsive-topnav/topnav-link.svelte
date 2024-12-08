<script lang="ts">
	import { page } from '$app/stores';

	export let href: string;
	export let responsive: boolean = false;
	$: pageHref = $page.url.href;
</script>

<a
	data-active={pageHref.includes(href)}
	class="float-left hidden px-[14px] py-4 text-lg text-[#f2f2f2] no-underline hover:bg-[#ddd] hover:text-black data-[active=true]:block data-[active=true]:bg-[#04aa6d] data-[active=true]:text-white sm:block"
	class:!float-none={responsive}
	class:!block={responsive}
	class:!text-left={responsive}
	{href}
>
	<slot></slot>
</a>
