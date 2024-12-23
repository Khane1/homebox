<script>
    /** @type {import('./$types').PageData} */
    export let data;
    let amenities = [
        { item: "Wifi", icon: `<i class="fa-solid fa-wifi"></i>` },
        { item: "Free parking", icon: `<i class="fa-solid fa-car"></i>` },
        { item: "Kitchen", icon: `<i class="fa-solid fa-kitchen-set"></i>` },
        { item: "Washer", icon: `<i class="fa-solid fa-clipboard-list"></i>` },
        { item: "TV or cable", icon: `<i class="fa-solid fa-tv"></i>` },
    ];
    let houserules = [
        " House rules for the guests",
        "Suitable for toddlers and children under 12.",
        "No unregistered guests allowed.",
        "Please don’t eat or drink in the bedrooms.",
        "Please take care of the furnishings. You have to pay for damages that exceed the security deposit.",
        "No illegal substances allowed on the premises.",
    ];
    let Landmarks = [
        "Universal™ Cinemark at Universal CityWalk Orlando",

        "The Simpsons Ride",

        "MEN IN BLACK Alien Attack",

        "Universal Studios Florida",

        "Hollywood Rip Ride Rockit",

        "Revenge of the Mummy",

        "Universal Orlando Resort",

        "The Incredible Hulk Coaster",

        "Dezerland Park Orlando",

        "Fun Spot America Theme Parks",

        "The Amazing Adventures of Spider-Man",

        "Universal Islands of Adventure",
    ];
    let y = 0;
</script>

<div class="h-full md:px-20">
    <div class="md:block hidden">
        <div class="w-full h-1/2 grid md:grid-cols-2 gap-2 mt-5">
            <div class="w-full h-full">
                <img
                    class="rounded-l-2xl object-cover"
                    src="https://images.trvl-media.com/lodging/1000000/800000/795900/795875/w3839h2563x0y4-3d3722ae.jpg?impolicy=resizecrop&rw=1200&ra=fit"
                    alt=""
                />
            </div>

            <div class="w-full h-full grid grid-cols-1 gap-2">
                <div class="">
                    <img
                        class="rounded-tr-2xl h-48 w-full object-cover"
                        src="https://images.trvl-media.com/lodging/1000000/800000/795900/795875/c4ab9786.jpg?impolicy=resizecrop&rw=1200&ra=fit"
                        alt=""
                    />
                </div>
                <div class="">
                    <img
                        class="rounded-br-2xl h-48 w-full object-cover"
                        src="https://images.trvl-media.com/lodging/1000000/800000/795900/795875/ddc94e02.jpg?impolicy=resizecrop&rw=1200&ra=fit"
                        alt=""
                    />
                </div>
            </div>
        </div>
    </div>

    <div class="md:hidden block">
        <div class="">
            <img
                class="rounded-2xl object-cover"
                src="https://images.trvl-media.com/lodging/1000000/800000/795900/795875/w3839h2563x0y4-3d3722ae.jpg?impolicy=resizecrop&rw=1200&ra=fit"
                alt=""
            />
        </div>
    </div>
    <div class="md:flex">
        <div class="md:w-4/5 w-full">
            <div class="pt-10 text-2xl font-semibold">
                Koki Hotel Family 2 bedroom
            </div>
            <div>4 Guests 2 Bedrooms 3 Beds 0 Bathroom</div>
            <div class="space-y-8 mt-6 mb-10">
                <div class="flex space-x-5">
                    <svg
                        id="Face"
                        width="24"
                        height="25"
                        viewBox="0 0 24 24"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            fill-rule="evenodd"
                            clip-rule="evenodd"
                            d="M12.25 4.13867C7.55558 4.13867 3.75 7.94425 3.75 12.6387C3.75 17.3331 7.55558 21.1387 12.25 21.1387C16.9444 21.1387 20.75 17.3331 20.75 12.6387C20.75 7.94425 16.9444 4.13867 12.25 4.13867ZM2.25 12.6387C2.25 7.11582 6.72715 2.63867 12.25 2.63867C17.7728 2.63867 22.25 7.11582 22.25 12.6387C22.25 18.1615 17.7728 22.6387 12.25 22.6387C6.72715 22.6387 2.25 18.1615 2.25 12.6387Z"
                            fill="#000000"
                        ></path>
                        <path
                            fill-rule="evenodd"
                            clip-rule="evenodd"
                            d="M8.75195 13.1899C8.75195 15.1217 10.318 16.6878 12.2498 16.6878C14.1816 16.6878 15.7476 15.1217 15.7476 13.1899H17.2476C17.2476 15.9502 15.01 18.1878 12.2498 18.1878C9.48956 18.1878 7.25195 15.9502 7.25195 13.1899H8.75195Z"
                            fill="#000000"
                        ></path>
                    </svg>
                    <div>Hosted by Koki Hotel</div>
                </div>
                <hr />
                <div class="mt-2 flex space-x-5 items-center">
                    <svg
                        id="Time Square"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                    >
                        <path
                            d="M15.68 20.991C19.973 20.22 21.5 17.636 21.5 12C21.5 5.063 19.187 2.75 12.25 2.75C5.313 2.75 3 5.063 3 12C3 18.937 5.313 21.25 12.25 21.25"
                            stroke="#000000"
                            stroke-width="1.5"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        ></path>
                        <path
                            d="M15.6403 14.0182L12.2493 11.9952V7.63416"
                            stroke="#000000"
                            stroke-width="1.5"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        ></path>
                    </svg>
                    <div>Check in time-flexible</div>
                </div>
                <hr />

                <div>
                    <div class="font-bold text-xl mb-5">About your host</div>
                    <div>
                        Casa Residences As a passionate lover of hospitality, I
                        thrive on creating memorable experiences that bring
                        people together. With a background in customer
                        experience, I believe that every detail matters when it
                        comes to crafting the perfect atmosphere. My journey in
                        hospitality has been fueled by a desire to connect
                        individuals and foster genuine relationships through
                        shared moments. Whether it’s organizing retreats,
                        hosting events, or curating unique experiences, I find
                        joy in ensuring that everyone feels welcomed and valued.
                        I’m dedicated to enhancing the well-being of others, and
                        I’m excited to help our customers revitalize their
                        spirits and connect . My goal is to create spaces where
                        laughter, joy, and lasting memories flourish.
                    </div>
                </div>
                <hr />
                <div class="font-bold text-xl">Amenities</div>
                <div class="grid grid-cols-3 gap-4">
                    {#each amenities as amenity}
                        <div class="flex space-x-5">
                            <div class="w-6 h-6">
                                {@html amenity.icon}
                            </div>
                            {amenity.item}
                        </div>
                    {/each}
                </div>
                <div class="">
                    <button class="border px-4 py-2 rounded-md">
                        More amenities
                    </button>
                </div>
                <div class="font-bold text-xl">Polices</div>
                <div class="grid md:grid-cols-2 gap-4">
                    <div>
                        <div class="font-semibold text-lg">House Rules</div>
                        <div class="space-y-2 my-5">
                            {#each { length: 4 } as rules, i}
                                <div>
                                    {houserules[i]}
                                </div>
                            {/each}
                            <div>
                                <button class="border px-4 py-2 rounded-md"
                                    >See More</button
                                >
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="font-semibold text-lg space-y-10">
                            Check in/out
                        </div>
                        <div>
                            Check in <span class="font-bold ml-10">10:00</span>
                        </div>
                        <div>
                            Check out <span class="font-bold ml-10">12:00</span>
                        </div>
                    </div>
                </div>
                <div class="mt-5">
                    <div class="font-semibold text-lg">Landmarks</div>
                    <div class="">
                        {#each { length: 4 } as landmark, i}
                            <div class="py-2">
                                {Landmarks[i]}
                            </div>
                        {/each}
                        <button class="border px-4 py-2 rounded-md"
                            >See More</button
                        >
                    </div>
                </div>
            </div>
        </div>
        <div class="pt-20 mx-10 w-1/2">
            <div
                class={y < 500
                    ? " hidden  "
                    : "md:fixed  top-20 fixed  w-2/4 md:block hidden"}
            >
                <div class="border md:w-1/2 rounded-lg px-10 py-5">
                    <div class="flex space-x-2">
                        <div class="font-semibold text-2xl">Ugx 200,000</div>
                        <div class="text-sm">night</div>
                    </div>

                    <div
                        class="border bg-yellow-400 font-bold rounded-lg px-10 py-5 my-10 text-center"
                    >
                        Book this location
                    </div>
                    <div></div>
                </div>
            </div>

            <div
                class="{y < 450
                    ? '  '
                    : ' hidden  '}  rounded-lg px-10 py-5 border"
            >
                <div class="flex space-x-2">
                    <div class="font-semibold text-2xl">Ugx 200,000</div>
                    <div class="text-sm">night</div>
                </div>
                <div class="mt-5"></div>
                <div>Guests</div>
                <div class="text-2xl flex space-x-5 items-center">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6 border rounded-full p-1 cursor-pointer"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M20 12H4"
                        />
                    </svg>
                    <div class="text-4xl font-bold">0</div>

                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="h-6 w-6 border rounded-full p-1 cursor-pointer"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                    >
                        <path
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            d="M12 6v6m0 0v6m0-6h6m-6 0H6"
                        />
                    </svg>
                </div>
                <div
                    class="border bg-yellow-400 font-bold rounded-lg px-10 py-5 my-10 text-center"
                >
                    Book this location
                </div>
            </div>
        </div>
    </div>
</div>
<div class=" bottom-0 left-0 py-5 fixed w-full md:hidden block bg-white border px-4">
    <div class="flex justify-between items-center">
        <div class="flex">
            <div class="font-semibold text-xl">Ugx 200,000</div>
            <div class="text-sm">night</div>
        </div>

            <button
            class="border bg-yellow-400 font-bold text-sm rounded-lg px-5 py-2 text-center"
            >
            Book
        </button>
    </div>
</div>

<svelte:window bind:scrollY={y} />
