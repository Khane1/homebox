<script>
    export let showsearchModal = false;
    import { categories } from "../../../utilities/categories";
    import Routingbtn from "../routingbuttons/routingbtn.svelte";
    let activeCategory = categories[0].category;
    $: search = "";
    import { page } from "$app/stores";
</script>

{#if showsearchModal}
    <div
        class="fixed inset-0 bg-black bg-opacity-50 z-20 flex items-center justify-start"
    >
        <div
            class="bg-white p-6 md:p-20 rounded-r-lg shadow-lg h-full md:w-3/5  w-full transition duration-500 delay-300"
        >
            <div class="flex justify-between items-center mb-4">
                <h2 class="md:text-2xl text-xl font-bold">
                    {#if $page.url.pathname != "/shop"}
                        <div>Where would you like to go?</div>
                    {:else}
                        <div>What are you looking for?</div>
                    {/if}
                </h2>
                <button
                    aria-label="close button"
                    class="text-gray-500 hover:text-gray-700"
                    on:click={() => (showsearchModal = false)}
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

            <div class="my-5">
                <hr />
            </div>
            <div class="flex md:w-1/2 justify-evenly  md:space-x-10 space-x-5 my-5">
                {#each categories as { category, icon }}
						<a href="/{category.toLowerCase()}">
							<Routingbtn
								activeCategory={$page.url.pathname.split(
									"/",
								)[1]}
								category={category.toLowerCase()}
								{icon}
							/>
						</a>
					{/each}
            </div>
            <div
                class="border px-4 py-3 flex rounded-t-xl items-center space-x-3"
            >
                <svg
                    id="Search"
                    width="24"
                    height="24"
                    viewBox="0 0 24 24"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                >
                    <path
                        d="M3.20972 10.789C3.20972 6.349 6.80872 2.75 11.2487 2.75C15.6877 2.75 19.2867 6.349 19.2867 10.789C19.2867 15.229 15.6877 18.828 11.2487 18.828C8.33572 18.828 5.78472 17.279 4.37472 14.96"
                        stroke="#000000"
                        stroke-width="1.5"
                        stroke-linecap="square"
                    ></path>
                    <path
                        d="M18.8845 18.856L21.2905 21.25"
                        stroke="#000000"
                        stroke-width="1.5"
                        stroke-linecap="square"
                    ></path>
                </svg>
                <input
                    type="text"
                    bind:value={search}
                    placeholder="Search"
                    class=" w-full focus:outline-none focus:ring-0 focus:border-white rounded-lg md:text-xl text-base"
                />
            </div>
            <div class="px-10 bg-slate-200 py-0.5"></div>
            {#if search.length > 0}
                <div class="px-5 bg-slate-50 py-5 rounded-b-lg space-y-3 md:text-lg text-base">
                    {#each { length: 2 } as a}
                        <a
                            href="/home"
                            on:click={() => (showsearchModal = false)}
                        >
                            <div
                                class="w-4/5 h-10 rounded cursor-pointer text-black"
                            >
                                {search}
                            </div>
                        </a>
                    {/each}
                </div>
            {/if}
            <div class="pt-10">Popular searches</div>
            <div class="space-y-4 mt-5">
                {#each { length: 4 } as search}
                    <div class="w-3/5 h-10 bg-slate-100 rounded"></div>
                {/each}
            </div>
        </div>
    </div>
{/if}
