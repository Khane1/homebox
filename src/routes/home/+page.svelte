<script>
    
    let selectedCurrency = "USD";
    let images = [
        {
            image: "https://images.trvl-media.com/lodging/1000000/800000/795900/795875/w3839h2563x0y4-3d3722ae.jpg?impolicy=resizecrop&rw=1200&ra=fit",
        },
        {
            image: "https://images.trvl-media.com/lodging/1000000/800000/795900/795875/c4ab9786.jpg?impolicy=resizecrop&rw=1200&ra=fit",
        },
        {
            image: "https://images.trvl-media.com/lodging/1000000/800000/795900/795875/ddc94e02.jpg?impolicy=resizecrop&rw=1200&ra=fit",
        },
    ];
</script>


<div class="grid lg:grid-cols-4 grid-cols-1 md:grid-cols-3 gap-10 mt-10">
    {#each { length: 12 } as card, i}
        <a href="/home/kireka">
            <div>
                <div class=" ">
                    <img
                        class="w-42 h-72 object-cover rounded-xl"
                        src={images[i % 3].image}
                        alt=""
                    />
                </div>
                <div class="font-semibold text-sm pt-3">
                    Hotel Flarmac Kireka
                </div>
                <div class="text-sm">
                    {selectedCurrency} 200000
                </div>
            </div>
        </a>
    {/each}
</div>
