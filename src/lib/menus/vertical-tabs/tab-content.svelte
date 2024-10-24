<script lang="ts">
	export let value: string;
	export let selected: string;
</script>

<div
	class="float-left h-screen w-[70%] border border-t-0 border-[#ccc] px-5 py-3"
	class:hidden={value !== selected}
>
	<slot />
</div>
