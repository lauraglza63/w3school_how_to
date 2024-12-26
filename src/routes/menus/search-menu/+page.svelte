<script Lang="ts">
	let list = [
		{ name: 'HTML', href: '#html' },
		{ name: 'CSS', href: '#css' },
		{ name: 'JavaScript', href: '#js' },
		{ name: 'PHP', href: '#php' },
		{ name: 'Python', href: '#python' },
		{ name: 'jQuery', href: '#jquery' },
		{ name: 'SQL', href: '#sql' },
		{ name: 'Bootstrap', href: '#bootstrap' },
		{ name: 'Node.js', href: '#node' }
	];

	let value = '';
	$: seachList = list.filter((item) => item.name.toLowerCase().includes(value.toLowerCase()));
</script>

<div class="flex">
	<div class="h-screen w-[30%] bg-[#bbb]">
		<p class="p-5 text-4xl">Menu</p>
		<input
			type="text"
			class="w-full border border-[#ddd] p-3 text-lg"
			placeholder="Search.."
			title="Type in a category"
			bind:value
		/>

		<ul class="m-0 list-none overflow-auto p-0">
			{#each seachList as item}
				<li>
					<a href={item.href} class="block p-3 text-black no-underline hover:bg-[#eee]"
						>{item.name}
					</a>
				</li>
			{/each}
		</ul>
	</div>

	<div class="bg-[#ddd] p-10">
		Lorem ipsum dolor sit, amet consectetur adipisicing elit. Temporibus itaque labore unde, ratione
		velit asperiores! Placeat molestiae totam eligendi voluptatum iure quas maxime officia ut nam
		consectetur. Sit, sunt quod!
	</div>
</div>
