<script>
    export const menu = ["Casas", "Apartamentos", "Lançamentos"];
</script>

<div class="hidden md:block">
    <div class="ml-10 flex items-baseline space-x-4 text-white">
        {#each menu as m}
        <a href="/{m}" class="hover:bg-gray-700 px-3 py-2 rounded-md text-base font-medium transition-300 ease-in-out">{m}</a>
        {/each}
    </div>
    
</div>