<script>
    import { onMount } from "svelte";
    import Verticlescroll from "../lib/components/buttons/verticalscroll/verticlescroll.svelte";

    let suggestions = [
        "https://images.trvl-media.com/lodging/1000000/800000/795900/795875/c4ab9786.jpg?impolicy=resizecrop&rw=1200&ra=fit",
        "https://a0.muscache.com/im/pictures/miso/Hosting-860808924365918973/original/380a9bea-4176-4f7b-9b78-224463786f56.jpeg?im_w=720",
        "https://a0.muscache.com/im/pictures/7db51ae5-3848-4f8e-87fa-3ec70c341e33.jpg?im_w=720",
        "https://a0.muscache.com/im/pictures/1b7e0c48-d3b0-4916-b7e3-a97d61774d11.jpg?im_w=720",
        "https://ak-d.tripcdn.com/images/0100x1200082c86ie1135_R_300_225_R5.jpg",
    ];

    let width = 0;

    let shoppingbag = width < 768 ? 60 : 100;
</script>

<div class="">
    <div class="md:text-6xl text-3xl my-10 md:my-32 text-center font-semibold">
        Our pleasure to serve you,
    </div>
    <div class="md:text-3xl mt-10 text-xl text-slate-800">Popular homes</div>
    <div>
        <div class="relative">
            <div class="flex gap-4 md:mt-10 mt-2 pb-4 overflow-hidden">
                {#each suggestions as item, i}
                    <a href="/home/suggestion">
                        <div
                            style="background-image: url('{item}');"
                            class="
                    object-cover bg-center bg-no-repeat bg-cover
                    flex-shrink-0 h-60 w-80 rounded-xl flex flex-col justify-end px-3 bg-slate-200 py-2 font-bold text-white"
                        >
                            Suggestion
                        </div>
                    </a>
                {/each}
            </div>
            <Verticlescroll cls=".overflow-hidden" />
        </div>
    </div>
    <div class="md:text-3xl text-xl font-bold md:mt-20 mt-10"></div>
    <div class="flex justify-center">
        <div class="md:flex md:justify-between space-x-2">
            <div class="md:w-1/2 flex items-center">
                <div
                    class="md:text-5xl text-2xl md:text-start text-center font-bold mt-10"
                >
                    Beautiful homes by amazing hosts
                </div>
            </div>

            <div class="md:w-full flex md:justify-center rounded-lg">
                <div
                    class="grid md:grid-cols-3 grid-cols-2 gap-4 group-hover:gap-10 md:mt-10 mt-5 pb-4 group"
                >
                    {#each { length: width < 768 ? 2 : 3 } as item, i}
                    <a href="/home/suggestion">
                        <div
                            style="background-image: url('{suggestions[
                                i + 1
                            ]}');"
                            class="
                        object-cover bg-center bg-no-repeat bg-cover
                        flex-shrink-0 h-96 md:w-64 w-40 transition-all duration-700 rounded-xl
                        flex flex-col justify-end px-3 bg-slate-200 py-2 font-bold text-white md:hover:!w-96"
                        >
                            Suggestion
                        </div>
                    </a>
                    {/each}
                </div>
            </div>
        </div>
    </div>
    <div class="md:text-3xl text-xl md:mt-44 mt-10 text-center">
        Travel to your dream destination
    </div>
    <div>
        <div class="flex overflow-hidden slick gap-4 md:mt-10 mt-5 pb-4">
            {#each suggestions as item, i}
            <a href="/home/suggestion">

                <div
                    style="background-image: url('{item}');"
                    class="
                    object-cover bg-center bg-no-repeat bg-cover
                    flex-shrink-0 h-80 w-96 rounded-xl flex flex-col justify-end px-3 bg-slate-200 py-2 font-bold text-white"
                >
                    Suggestion
                </div>
            </a>
            {/each}
        </div>
        <div>
            <Verticlescroll cls=".slick" />
        </div>
    </div>
    <div>
        <div
            class="md:text-lg text-base text-gray-600 text-center max-w-2xl mx-auto mt-4"
        >
            Discover breathtaking destinations, immerse yourself in diverse
            cultures, and create unforgettable memories. Whether you're seeking
            adventure or relaxation, your perfect journey awaits.
        </div>
    </div>
    <div class="md:flex md:justify-center mt-20">
        <div class="md:flex md:justify-between space-x-2">
            <div class="md:w-full flex md:justify-center rounded-lg">
                <div
                    class="grid md:grid-cols-3 grid-cols-2 gap-4 group-hover:gap-10 md:mt-10 mt-5 pb-4 group"
                >
                    {#each { length: width < 768 ? 2 : 3 } as item, i}
                        <div
                            style="background-image: url('{suggestions[
                                i + 1
                            ]}');"
                            class="
                        object-cover bg-center bg-no-repeat bg-cover
                        flex-shrink-0 h-96 md:w-64 w-40 transition-all duration-700 rounded-xl
                        flex flex-col justify-end px-3 bg-slate-200 py-2 font-bold text-white md:hover:!w-96"
                        >
                            Suggestion
                        </div>
                    {/each}
                </div>
            </div>
        </div>
        <!-- <div class="md:w-1/2 flex items-center justify-center">
            <div
                class="md:text-5xl text-2xl flex items-end space-x-3 md:font-bold font-semibold mt-10"
            >
                Market day is <br />shopping day! ✨<svg
                    id="Bag"
                    width={shoppingbag}
                    height={shoppingbag}
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
            </div>
        </div> -->
    </div>
    <div>
        <div class="md:px-20 px-4 md:py-16 py-8">
            <div class="grid md:grid-cols-3 gap-8">
                <div class="text-center">
                    <h3 class="md:text-2xl text-xl font-semibold mb-4">
                        Business Exposure
                    </h3>
                    <p class="text-gray-600">
                        We engage with local businesses to showcase their
                        products and reach a wider customer base.
                    </p>
                </div>
                <div class="text-center">
                    <h3 class="md:text-2xl text-xl font-semibold mb-4">
                        Revenue Growth
                    </h3>
                    <p class="text-gray-600">
                        Our market days create opportunities for businesses to
                        increase sales and build lasting customer relationships
                        in their community.
                    </p>
                </div>
                <div class="text-center">
                    <h3 class="md:text-2xl text-xl font-semibold mb-4">
                        Youth Empowerment
                    </h3>
                    <p class="text-gray-600">
                        We support young entrepreneurs by providing them with a
                        platform to launch and grow their businesses in a
                        supportive environment.
                    </p>
                </div>
            </div>
        </div>
    </div>
    <div class="md:my-32 my-20 md:text-4xl text-xl font-base text-center">
        We've got something for everyone,<br />
        join the Faith Homes family today
    </div>
    <div>
        <div class="flex justify-center gap-4 mb-20">
            <a
            href="/home"
                class="bg-black text-white md:px-8 px-4 py-2 md:py-4 rounded-full hover:bg-gray-800 transition-colors"
            >
                Get Started
            </a>
            <a
                href="/home"
                class="border border-black md:px-8 px-4 py-2 md:py-4 rounded-full hover:bg-gray-100 transition-colors"
            >
                Explore homes
            </a>
        </div>
    </div>
</div>
<svelte:window bind:innerWidth={width} />

<style>
    .image {
        background-image: url();
        object-fit: contain;
    }
</style>
