<script>
    export let cls=""

</script>

<div class="flex justify-end">
    <button
        class="  transform bg-white p-2 rounded-full shadow-lg"
        aria-label="Scroll left"
        on:click={() => {
            const container =
                document.querySelector(cls);
            container.scrollBy({ left: -300, behavior: "smooth" });
        }}
    >
        <svg
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
                d="M15 19l-7-7 7-7"
            />
        </svg>
    </button>
    <button
        class=" bg-white p-2 rounded-full shadow-lg"
        aria-label="Scroll right"
        on:click={() => {
            const container =
                document.querySelector(cls);
            container.scrollBy({ left: 300, behavior: "smooth" });
        }}
    >
        <svg
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
                d="M9 5l7 7-7 7"
            />
        </svg>
    </button>
</div>