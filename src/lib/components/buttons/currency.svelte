<script>
    import { currencies } from "../../utilities/currencies";
    export let selectedCurrency = currencies[0];
    export let showModal = false;
</script>

{#if showModal}
    <div
        class="fixed  inset-0 bg-black bg-opacity-50 z-20 flex items-center justify-center overflow-y-auto"
    >
        <div
            class="bg-white p-6 md:p-20 0 md:pt-20 rounded-lg shadow-lg md:w-3/4 h-auto mx-4 my-8 max-h-[90vh] overflow-y-auto"
        >
            <div class="flex justify-between items-center mb-4">
                <h2 class="text-2xl font-bold">Select Currency</h2>
                <button
                    aria-label="close button"
                    class="text-gray-500 hover:text-gray-700"
                    on:click={() => (showModal = false)}
                    ><svg
                        aria-label="close button"
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M6 18L18 6M6 6l12 12"
                        />
                    </svg></button
                >
            </div>
            <div class=" font-semibold text-blue-700 mb-4 text-sm mt-5">Most Used</div>
            <div class=" grid md:grid-cols-3 grid-cols-1 gap-5 mt-2 text-slate-900">
                {#each { length: 3 } as val, i}
                    <button
                        class="w-full text-xs   text-left p-2  hover:bg-gray-100 rounded"
                        on:click={() => {
                            selectedCurrency = currencies[i].currency;
                            showModal = false;
                        }}
                        ><span class="font-bold"
                            >{currencies[i].currency} -
                            <span class="font-normal">
                                {currencies[i].name}
                            </span>
                        </span>
                    </button>
                {/each}
            </div>
            <div class="my-5">
                <hr />
            </div>
            <div class="font-semibold text-blue-700 mb-4 text-sm">
                All currencies
            </div>
            <div class=" grid md:grid-cols-4 grid-cols-2 gap-5 text-slate-900">
                {#each currencies as { currency, name }}
                    <button
                        class="w-full text-xs text-left p-2 hover:bg-gray-100 rounded"
                        on:click={() => {
                            selectedCurrency = currency;
                            showModal = false;
                        }}
                        ><span class="font-bold">{currency}</span> - {name}</button
                    >
                {/each}
            </div>
        </div>
    </div>{/if}
