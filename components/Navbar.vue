<template>
	<nav class="mx-8">
		<div class="max-w-full flex flex-row flex-nowrap items-center justify-between p-4">
			<div class="flex flex-row items-baseline gap-2 lg:gap-10">
				<NuxtLink to="/" class="flex items-center justify-center px-4 md:px-6 py-1.5 rounded-3xl header-logo-bg">
					<img src="~/assets/svg/header.svg" class="h-4 mr-2 " />
					<span class="self-center text-base font-semibold whitespace-nowrap text-white">Menu</span>
				</NuxtLink>

				<div id="navbarLink">
					<ul
						class="hidden md:flex md:flex-row items-center flex-nowrap md:gap-4 lg:gap-8 text-white md:text-black font-medium p-4">
						<li>
							<a href="#">Platform</a>
						</li>
						<li>
							<a href="#">Feature</a>
						</li>
						<li>
							<a href="#">Integration</a>
						</li>
						<li>
							<a href="#">Pricing</a>
						</li>
						<li>
							<a href="#">Changelog</a>
						</li>
					</ul>
				</div>
			</div>
			<div id="navbarBtn">
				<div class="hidden md:flex flex-row flex-nowrap gap-10 md:gap-3 items-center md:ml-4">
					<button type="button"
						class="text-black bg-white border font-medium rounded-3xl whitespace-nowrap text-lg md:text-sm px-8 md:px-5 py-2 text-center">
						Sign up
					</button>
					<button type="button"
						class="text-white font-medium rounded-3xl text-lg md:text-sm px-8 md:px-5 py-2 text-center gradient-button">
						Login
					</button>
				</div>
			</div>

			<div id="closeOverlay" class="text-white">
				<button type="button" v-on:click="expandNav">&times;</button>
			</div>
			<button data-collapse-toggle="navbarLink" type="button" v-on:click="expandNav"
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
			let nav = document.getElementById("navbarLink");
			let navBtn = document.getElementById("navbarBtn");
			let closeBtn = document.getElementById("closeOverlay");

			if (nav.className === "") {
				nav.className += " overlay";
				nav.style.height = "100%";
				navBtn.className += " overlay-btn";
				closeBtn.style.display = "block";
			} else {
				nav.style.height = "0%";
				navBtn.className = "";
				closeBtn.style.display = "none";
				nav.className = "";
			}
		}
	}
}
</script>

<style scoped>
@import url("~/assets/css/navbar.css");
</style>
