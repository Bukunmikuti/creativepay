<template>
	<nav class="mx-8">
		<div class="max-w-full flex flex-row items-center justify-between mx-auto p-4">
			<NuxtLink to="/" class="flex items-center justify-center px-6 py-1.5 rounded-3xl header-logo-bg">
				<img src="~/assets/svg/header.svg" class="h-4 mr-2 " />
				<span class="self-center text-base font-semibold whitespace-nowrap text-white">Menu</span>
			</NuxtLink>

			<div class="" id="navbar-cta">
				<ul class="hidden md:flex md:flex-row md:gap-8 font-medium p-4 mt-4">
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

			<div class="flex md:order-2 md:hidden">
				<button data-collapse-toggle="navbar-cta" type="button" v-on:click="expandNav"
					class="inline-flex items-center p-2 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100">
					<span class="sr-only">Open main menu</span>
					<svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg">
						<path fill-rule="evenodd"
							d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
							clip-rule="evenodd"></path>
					</svg>
				</button>
			</div>
			<div class="flex flex-row items-center justify-center gap-9">
				<button type="button" class="text-black border font-medium rounded-3xl text-sm px-5 py-2 text-center">
					Sign up
				</button>
				<button type="button"
					class="text-white font-medium rounded-3xl text-sm px-5 py-2 text-center gradient-button">
					Login
				</button>
			</div>
		</div>
		<hr class="mx-auto w-full" />
	</nav>

	<!-- <nav class="bg-white border-gray-200">
		<div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
		</div>
	</nav> -->
</template>

<script>
export default {
	methods: {
		expandNav: function () {
			let nav = document.getElementById("navbar-cta");

			if (nav.className === "") {
				nav.className += " overlay";
				nav.style.height = "100%";
				console.log(nav.childNodes);
			} else {
				nav.className = "";
				nav.style.height = "0%";
			}
		}
	}
}
</script>

<style scoped>
@import url("~/assets/css/navbar.css");

.overlay {
	height: 0%;
	width: 100%;
	position: fixed;
	z-index: 1;
	left: 0;
	top: 0;
	background-color: black;
	background-color: rgba(0, 0, 0, 0.8);
	overflow-x: hidden;
	transition: 0.5s;
}

.overlay ul {
	position: relative;
	top: 25%;
	width: 100%;
	text-align: center;
	margin-top: 30px;
	color: white;
}

.overlay li {
	padding: 8px;
	text-decoration: none;
	display: block;
	transition: 0.3s;
}
</style>
