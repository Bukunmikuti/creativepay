<template>
	<nav class="bg-white border-gray-200">
		<div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
			<NuxtLink to="/" class="flex items-center p-1.5 mr-3 px-4 rounded-3xl header-logo-bg">
				<img src="~/assets/images/header.svg" class="h-4 mr-2 " />
				<span class="self-center text-lg font-semibold whitespace-nowrap dark:text-white">Menu</span>
			</NuxtLink>
			<div class="flex md:order-2">
				<button type="button"
					class="text-black border focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-3xl text-sm px-5 py-2 text-center mr-3 md:mr-0">
					Sign up
				</button>
				<button type="button"
					class="text-white focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-3xl text-sm px-5 py-2 text-center mr-3 md:mr-0 gradient-button">
					Login
				</button>
				<button data-collapse-toggle="navbar-cta" type="button"
					class="inline-flex items-center p-2 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
					aria-controls="navbar-cta" aria-expanded="false">
					<span class="sr-only">Open main menu</span>
					<svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg">
						<path fill-rule="evenodd"
							d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
							clip-rule="evenodd"></path>
					</svg>
				</button>
			</div>
			<div class="items-center mr-auto justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-cta">
				<ul
					class="flex flex-col font-medium p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-white">
					<li>
						<a href="#"
							class="text-opacity-70 block py-2 pl-3 pr-4 text-black md:hover:text-blue-700 md:p-0">Platform</a>
					</li>
					<li>
						<a href="#"
							class="text-opacity-70 block py-2 pl-3 pr-4 text-black md:hover:text-blue-700 md:p-0">Feature</a>
					</li>
					<li>
						<a href="#"
							class="text-opacity-70 block py-2 pl-3 pr-4 text-black md:hover:text-blue-700 md:p-0">Integration</a>
					</li>
					<li>
						<a href="#"
							class="text-opacity-70 block py-2 pl-3 pr-4 text-black md:hover:text-blue-700 md:p-0">Pricing</a>
					</li>
					<li>
						<a href="#"
							class="text-opacity-70 block py-2 pl-3 pr-4 text-black md:hover:text-blue-700 md:p-0">Changelog</a>
					</li>
				</ul>
			</div>
		</div>
		<hr class="mx-auto w-11/12" />
	</nav>
</template>

<script>
export default {
	data() {
		return {
		}
	}
}
</script>

<style scoped>
.header-logo-bg {
	background: linear-gradient(102.06deg, #6260DD -48.23%, #21242E -1.34%, #6260DD 110.35%, #21242E 164.91%);
}

.gradient-button {
	background: linear-gradient(90.81deg, #6260DD -43.97%, #43437A 160.54%);
	background-blend-mode: darken;
}
</style>
