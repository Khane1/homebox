<script>
    let suggestions = [
        {
            image: "https://fashionclinik.com/wp-content/uploads/2023/12/Sneaker-Shoes-for-Men1.jpg",
            title: "Running Shoes ",
            price: 50000,
            category: "Shoes",
        },
        {
            image: "https://m.media-amazon.com/images/I/71Bzs7x0ZlL._SL1500_.jpg",
            title: "Black Soap",
            price: 25000,
            category: "Soap",
        },
        {
            image: "https://i5.walmartimages.com/seo/Ariana-Grande-Sweet-Like-Candy-Eau-de-Parfum-Perfume-for-Women-1-Oz_6e8a4fdb-601f-42e5-86b0-0ed64fb1412a.28b228882edbbd27cf7d851dad8ec0df.jpeg",
            title: "Exil Perfume",
            price: 15000,
            category: "Perfume",
        },
        {
            image: "https://s3-media0.fl.yelpcdn.com/bphoto/T4NzMCiho8KcFG8DFKPteg/348s.jpg",
            title: "Flat pinkies",
            price: 43000,
            category: "Shoes",
        },
        {
            image: "https://5.imimg.com/data5/SELLER/Default/2022/11/YV/ZF/YO/116453489/white-casual-shoes-for-men.jpg",
            title: "Cool sneakers",
            price: 65000,
            category: "Shoes",
        },
        {
            image: "https://m.media-amazon.com/images/I/71cr6bO8OpL._SL1500_.jpg",
            title: "Black Soap | 250grams",
            price: 80000,
            category: "Soap",
        },
        {
            image: "https://target.scene7.com/is/image/Target/GUEST_81b505e6-0808-4079-87ef-c459407aa1a2?wid=488&hei=488&fmt=pjpeg",
            title: "Pure essencial T-tree Oils",
            price: 15000,
            category: "Oils",
        },
        {
            image: "https://gomatic.co.uk/cdn/shop/products/Gomatic_Messenger_AngleFront_20190702.jpg?v=1631017350&width=1080",
            title: "Side bags",
            price: 150000,
            category: "Bags",
        },
        {
            image: "https://d1q03ajwgi7cv2.cloudfront.net/media/catalog/category/REGENT-0022511120007487_Side.jpg",
            title: "HandBag",
            price: 30000,
            category: "Bags",
        },
        {
            image: "https://www.smartertravel.com/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2019/06/plae-crosby-flat-shoes-1400x500.png.webp",
            title: "Side bags",
            price: 150000,
            category: "Bags",
        },
        {
            image: "https://thumbs.dreamstime.com/b/trekking-shoes-traverse-mountainous-area-as-hiker-conquers-hilltop-generative-ai-279635501.jpg",
            title: "Boots",
            price: 30000,
            category: "Bags",
        },
    ];
    let categories = [
        {
            name: "Aparel",
            icon: "fa-shirt text-violet-600",
            link: "/shop/clothing ",
        },
        {
            name: "Shoes",
            icon: "fa-shoe-prints text-orange-600",
            link: "/shop/shoes",
        },
        {
            name: "Bags",
            icon: "fa-bag-shopping text-pink-600",
            link: "/shop/bags",
        },
        {
            name: "Oils",
            icon: "fa-oil-can text-cyan-600",
            link: "/shop/perfumes",
        },
        {
            name: "Perfume",
            icon: "fa-spray-can-sparkles text-red-600",
            link: "/shop/perfumes",
        },
        {
            name: "Discounts%",
            icon: "fa-tag text-green-600",
            link: "/shop/perfumes",
        },
    ];
    let width = 0;
    let selectedCategory = "";
</script>

<div class="flex justify-center">
    <div class="grid md:grid-cols-6 grid-cols-3 w-full lg:w-1/3">
        {#each categories as item, i}
            <button
                on:click={() => {
                    selectedCategory = item.name;
                }}
            >
                <div class="flex justify-center my-2 cursor-pointer">
                    <div
                        class="rounded-full w-10 h-10 md:w-12 md:h-12 flex items-center justify-center bg-white shadow hover:shadow-xl"
                    >
                        <i class="fa-solid {item.icon}"></i>
                    </div>
                </div>
                <div class="text-center text-xs">
                    {item.name}
                </div>
            </button>
        {/each}
    </div>
</div>

{#if selectedCategory == ""||selectedCategory == "Discounts%"}
    <div class="md:text-3xl text-xl md:my-20 mt-10 font-bold">
        Discover Amazing Deals %
    </div>
    <div class="columns-2 sm:columns-2 md:columns-3 lg:columns-5 gap-6 pb-6">
        {#each { length: 5 } as item, i}
            <div>
                <div
                    style="background-image: url('{suggestions[
                        i % suggestions.length
                    ]
                        .image}'); background-size: cover; background-position: center;"
                    class=" break-inside-avoid relative overflow-hidden object-fill my-6 rounded-xl hover:scale-105 transition-transform duration-300"
                >
                    <div
                        class="w-full bg-cover bg-center bg-no-repeat"
                        style="height: {i % 2 === 0 ? '250px' : '350px'}"
                    >
                        <div
                            class="absolute bottom-0 left-0 right-0 p-3 bg-gradient-to-t from-black/50 to-transparent"
                        >
                            <div class="flex justify-between">
                                <div>
                                    <div>
                                        <span
                                            class="font-bold text-sm text-white"
                                            >{suggestions[
                                                i % suggestions.length
                                            ].title}
                                            ..</span
                                        >
                                    </div>
                                    <div>
                                        <span class="text-xs text-white"
                                            >Ugx</span
                                        >
                                        <span
                                            class="font-semibold text-xl text-orange-500 line-through"
                                            >{suggestions[
                                                i % suggestions.length
                                            ].price}</span
                                        >
                                        <span
                                            class="font-extrabold text-xl text-white ml-2"
                                            >{Math.floor(
                                                suggestions[
                                                    i % suggestions.length
                                                ].price * 0.8,
                                            )}</span
                                        >
                                    </div>
                                </div>
                                <div class="">
                                    <button
                                        aria-label="Add to cart"
                                        on:click={() => {
                                            console.log("clicked");
                                        }}
                                        class="rounded-full bg-white p-4 shadow-xl"
                                    >
                                        <svg
                                            id="Bag"
                                            width="24"
                                            height="24"
                                            viewBox="0 0 24 24"
                                            fill="none"
                                            xmlns="http://www.w3.org/2000/svg"
                                        >
                                            <path
                                                d="M3.41547 15.9348C2.74727 20.3924 5.09968 21.5 8.16604 21.5H16.5139C19.5802 21.5 21.8686 19.889 21.3011 15.9348L20.523 9.89357C20.047 7.73339 18.7107 6.81805 17.4475 6.81805H7.26901C6.02416 6.81805 4.6054 7.66931 4.1935 9.89357L3.87473 12.3687"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M16.6513 6.59839C16.6513 4.21232 14.717 2.27802 12.331 2.27802C11.182 2.27315 10.0783 2.72618 9.26416 3.53694"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M15.2965 11.1018H15.2507"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M9.4659 11.1018H9.42013"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                        </svg>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class=""></div>
            </div>
        {/each}
    </div>
{/if}
<div class="md:text-3xl text-xl md:my-20 mt-10 font-bold">
    {#if selectedCategory != ""}
        {selectedCategory}
         <button 
         class="rounded-full shadow-lg p-2 bg-white"
         on:click={() => {
            selectedCategory = "";
        }}
         aria-label="Clear selection">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" 
            fill="#DC2626" stroke="#DC2626" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <line x1="18" y1="6" x2="6" y2="18"></line>
                <line x1="6" y1="6" x2="18" y2="18"></line>
            </svg>
        </button>
    {:else}
        Discover Unique Treasures & Local Gems
    {/if}
</div>

<div class="columns-2 sm:columns-2 md:columns-3 lg:columns-4 md:gap-6 pb-6">
    {#each { length: suggestions.length * 7 } as item, i}
        {#if selectedCategory == suggestions[i % suggestions.length].category || selectedCategory == ""}
            <div>
                <div
                    style="background-image: url('{suggestions[
                        i % suggestions.length
                    ]
                        .image}'); background-size: cover; background-position: center;"
                    class=" break-inside-avoid relative overflow-hidden  md:object-fill my-6 rounded-xl hover:scale-105 transition-transform duration-300"
                >
                    <div
                        class="w-full bg-cover bg-center bg-no-repeat"
                        style="height: {i % 2 === 0 ? '250px' : '350px'}"
                    >
                        <div
                            class="absolute bottom-0 left-0 right-0 p-3 bg-gradient-to-t from-black/50 to-transparent"
                        >
                            <div class="flex justify-between">
                                <div>
                                    <div>
                                        <span
                                            class="font-bold text-sm text-white"
                                            >{suggestions[
                                                i % suggestions.length
                                            ].title}
                                            ..</span
                                        >
                                    </div>
                                    <div>
                                        <span class="text-xs text-white"
                                            >Ugx</span
                                        >
                                        <span
                                            class="font-extrabold text-xl text-white"
                                            >{suggestions[
                                                i % suggestions.length
                                            ].price}</span
                                        >
                                    </div>
                                </div>
                                <div class="">
                                    <button
                                        aria-label="Add to cart"
                                        on:click={() => {
                                            console.log("clicked");
                                        }}
                                        class="rounded-full bg-white p-4 shadow-xl"
                                    >
                                        <svg
                                            id="Bag"
                                            width="24"
                                            height="24"
                                            viewBox="0 0 24 24"
                                            fill="none"
                                            xmlns="http://www.w3.org/2000/svg"
                                        >
                                            <path
                                                d="M3.41547 15.9348C2.74727 20.3924 5.09968 21.5 8.16604 21.5H16.5139C19.5802 21.5 21.8686 19.889 21.3011 15.9348L20.523 9.89357C20.047 7.73339 18.7107 6.81805 17.4475 6.81805H7.26901C6.02416 6.81805 4.6054 7.66931 4.1935 9.89357L3.87473 12.3687"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M16.6513 6.59839C16.6513 4.21232 14.717 2.27802 12.331 2.27802C11.182 2.27315 10.0783 2.72618 9.26416 3.53694"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M15.2965 11.1018H15.2507"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                            <path
                                                d="M9.4659 11.1018H9.42013"
                                                stroke="#000000"
                                                stroke-width="1.5"
                                                stroke-linecap="round"
                                                stroke-linejoin="round"
                                            ></path>
                                        </svg>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class=""></div>
            </div>
        {/if}
    {/each}
</div>
<svelte:window bind:innerWidth={width} />
