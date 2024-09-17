<script>
	import MobileMenu from './MobileMenu.svelte';
	import logo from '$lib/imagens/logo.png';
	import Menu from './Menu.svelte';

  	import menu from './MobileMenu.svelte';
	import Button from './Button.svelte';

  let isOpen = false;
</script>

<header>
	<nav class="bg-slate-500">
		<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
			<div class="flex items-center justify-around h-32 2xl:justify-between">
				<div class="flex items-center">
					<a href="/" class="shrink-0">
						<img src={logo} alt="logo da Sonhar Vitória Imóveis" class="h-32 w-auto" />
					</a>
					<Menu />
				</div>
				<div class="flex gap-4">
					<Button href={"anuncie"}>Anuncie</Button>
					<Button href={"contato"}>Contato</Button>
				</div>
				<div class="-mr-2 flex md:hidden">
					<button
						id="menuButton"
						type="button"
						class="inline-flex items-center justify-center p-2 rounded-md text-gray-800 hover:text-white hover:bg-gray-700 focus:outline-none focus:bg-gray-700 focus:text-white transition-300 ease-in-out"
						aria-label="Menu"
						aria-expanded="false"
						on:click={() => (isOpen = !isOpen)}
					>
						<svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M4 6h18M4 12h16M4 18h16"
							></path>
						</svg>
					</button>
				</div>
			</div>
		</div>
	{#if isOpen}	
    	<MobileMenu />
	{/if}

	</nav>
</header>

<style>
</style>
