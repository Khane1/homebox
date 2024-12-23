<script>
	import "../app.css";
	import "../layout.css";
	import Currency from "../lib/components/buttons/currency.svelte";
	import { currencies } from "../lib/utilities/currencies";

	let showModal = false;
	let selectedCurrency = currencies[1].currency;
	import { categories } from "../lib/utilities/categories";
	let activeCategory = categories[0].category;
	import { page } from "$app/stores";
	import Search from "../lib/components/buttons/search/search.svelte";
	import Routingbtn from "../lib/components/buttons/routingbuttons/routingbtn.svelte";
	let currentpage = 1;
	let showsearchModal = false;
	let showMenu = false;
</script>

<div class="flex h-fit md:mx-20 mx-5">
	<div class=" my-4 w-full">
		<div class="flex items-center justify-between p-2 rounded">
			<a href="/">
				<div class="flex">
					<div
						class="w-8 h-8 p-1 bg-yellow-400 rounded-lg font-bold"
						alt="">
						HB
				</div>
					<div class="text-2xl font-bold ml-2 text-slate-900">
					HomeBox
					</div>
				</div>
			</a>

			<div class="md:block hidden">
				<button
					on:click={() => {
						showsearchModal = true;
					}}
					class="pr-32 text-sm items-center text-slate-500 pl-4 py-3 space-x-3 text-end rounded-full border flex"
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
					{#if $page.url.pathname != "/shop"}
						<div>Where would you like to go?</div>
					{:else}
						<div>What are you looking for?</div>
					{/if}
				</button>
			</div>
			<div class=" flex">
				<button
					class=" lg:block hidden text-sm font-bold px-5 mx-2 py-2 text-slate-600 hover:text-blue-600"
				>
					Share your home
				</button>

				<div class="relative block lg:hidden ">
					<button
						aria-label="Toggle menu"
						on:click={() => (showMenu = !showMenu)}
						class="p-2 rounded-full hover:bg-gray-100"
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
								d="M4 6h16M4 12h16M4 18h16"
							/>
						</svg>
					</button>

					{#if showMenu}
						<div
							class="absolute right-0 mt-2  bg-white rounded-md shadow-lg py-1 w-48 z-50"
						>
						<button
							class="block px-4 py-2 text-base text-gray-700 hover:bg-gray-100 w-full text-start"
							on:click={() => (showsearchModal = true,showMenu = false)}
							>Search</button
						>
							<button
								class="block px-4 py-2 text-base text-gray-700 hover:bg-gray-100  w-full text-start"
								on:click={() => (showModal = true,showMenu = false)}
								>Select currency</button
							>
							
							
							<hr class="my-1" />
							<a
							on:click={() => (showMenu = false)}

								href="/"
								class="block px-4 py-2 text-base text-gray-700 hover:bg-gray-100  w-full text-start"
								>Share your home</a
							>
							
						</div>
					{/if}
				</div>

				<button
					class="p-2 rounded-lg border-2 text-xs font-bold hidden md:block"
					on:click={() => (showModal = true)}
					>{selectedCurrency}</button
				>

				<Currency bind:showModal bind:selectedCurrency />
				<Search bind:showsearchModal />
			</div>
		</div>
		<div class="mb-8"></div>

		{#if ($page.url.pathname != "/" && $page.url.pathname != "/shop" && $page.url.pathname == "/home") || $page.url.pathname == "/experience" || $page.url.pathname == "/event"}
			<div class="flex justify-center">
				<div class="grid grid-cols-4 gap-10">
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
			</div>
		{/if}
		<slot />
	</div>

	<div></div>
</div>
{#if $page.url.pathname == "/"}
	<footer class="bg-gray-100 py-20 mt-auto mt-20 bottom-0 w-full">
		<div class="container mx-auto px-4">
			<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
				<div>
					<h3 class="font-bold text-lg mb-4">Support</h3>
					<ul class="space-y-2">
						<li>
							<a
								href="/help"
								class="text-gray-600 hover:text-blue-600"
								>Help Center</a
							>
						</li>
						<li>
							<a
								href="/safety"
								class="text-gray-600 hover:text-blue-600"
								>Safety Information</a
							>
						</li>
						<li>
							<a
								href="/cancellation"
								class="text-gray-600 hover:text-blue-600"
								>Cancellation Options</a
							>
						</li>
					</ul>
				</div>
				<div>
					<h3 class="font-bold text-lg mb-4">Community</h3>
					<ul class="space-y-2">
						<li>
							<a
								href="/disaster-relief"
								class="text-gray-600 hover:text-blue-600"
								>Disaster Relief</a
							>
						</li>
						<li>
							<a
								href="/support"
								class="text-gray-600 hover:text-blue-600"
								>Support Refugees</a
							>
						</li>
						<li>
							<a
								href="/diversity"
								class="text-gray-600 hover:text-blue-600"
								>Celebrating Diversity</a
							>
						</li>
					</ul>
				</div>
				<div>
					<h3 class="font-bold text-lg mb-4">Hosting</h3>
					<ul class="space-y-2">
						<li>
							<a
								href="/host"
								class="text-gray-600 hover:text-blue-600"
								>Try Hosting</a
							>
						</li>
						<li>
							<a
								href="/protection"
								class="text-gray-600 hover:text-blue-600"
								>Host Protection</a
							>
						</li>
						<li>
							<a
								href="/community"
								class="text-gray-600 hover:text-blue-600"
								>Community Forum</a
							>
						</li>
					</ul>
				</div>
				<div>
					<h3 class="font-bold text-lg mb-4">About</h3>
					<ul class="space-y-2">
						<li>
							<a
								href="/about"
								class="text-gray-600 hover:text-blue-600"
								>About Us</a
							>
						</li>
						<li>
							<a
								href="/careers"
								class="text-gray-600 hover:text-blue-600"
								>Careers</a
							>
						</li>
						<li>
							<a
								href="/press"
								class="text-gray-600 hover:text-blue-600"
								>Press Center</a
							>
						</li>
					</ul>
				</div>
			</div>
			<div
				class="border-t border-gray-200 mt-8 pt-8 flex flex-col md:flex-row justify-between items-center"
			>
				<div class="flex space-x-6 mb-4 md:mb-0">
					<a href="/terms" class="text-gray-600 hover:text-blue-600"
						>Terms</a
					>
					<a href="/privacy" class="text-gray-600 hover:text-blue-600"
						>Privacy</a
					>
					<a href="/sitemap" class="text-gray-600 hover:text-blue-600"
						>Sitemap</a
					>
				</div>
				<div class="text-gray-600">
					© 2023 Tubayo, Inc. All rights reserved.
				</div>
			</div>
		</div>
	</footer>
{/if}
