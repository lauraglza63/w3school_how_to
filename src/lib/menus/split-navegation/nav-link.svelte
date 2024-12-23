<script lang="ts">
	export let href = '';
	export let align: 'left' | 'right' = 'left';
</script>

<a
	{href}
	data-align={align}
	class="px-[14px] py-4 text-center text-lg text-[#f2f2f2] no-underline hover:bg-[#ddd] hover:text-black data-[align=right]:float-right data-[align=left]:float-left data-[align=right]:bg-[#04aa6d] hover:data-[align=right]:bg-[#ddd]"
>
	<slot></slot>
</a>
