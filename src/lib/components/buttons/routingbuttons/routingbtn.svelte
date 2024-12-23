<script>
    export let category,activeCategory,icon;
</script>
<button on:click={() => (activeCategory = category)}>
    <div
        class="flex flex-col items-center group transition delay-200 transform duration-200"
    >
        <div
            class=" {activeCategory == category
                ? ' font-semibold '
                : 'text-slate-500  group-hover:text-slate-800'}   mb-2 text-sm flex items-center justify-center"
        >
            {@html icon}
        </div>
        <div
            class=" text-xs {activeCategory == category
                ? 'font-semibold'
                : ''} flex justify-center mb-2 capitalize"
        >
            {category}s
        </div>
        <div
            class=" px-5 py-0.5 {activeCategory ==
            category
                ? 'block bg-slate-300'
                : 'bg-slate-200 group-hover:block hidden'} "
        ></div>
    </div>
</button>