<script>
	const menuItens = ['Casas', 'Apartamentos', 'Lançamentos', 'Anuncie', 'Contato'];

</script>

<div id="menu" class="md:hidden">
	<div class="px-2 pt-2 pd-3 sm:px-3">
		{#each menuItens as m}
			<a
				href="/{m}"
				class="hover:bg-gray-700 text-white block px-3 py-2 rounded-md text-base font-medium
            transition-300 ease-in-out">{m}</a
			>
		{/each}
	</div>
</div>
