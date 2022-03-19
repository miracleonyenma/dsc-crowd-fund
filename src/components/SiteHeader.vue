<script setup>
	import { RouterLink, RouterView } from "vue-router";
</script>
<template>
	<header>
		<div class="wrapper">
			<figure class="logo">
				<RouterLink to="/">
					<h1>Web3 Funds</h1>
				</RouterLink>
			</figure>
			<nav>
				<ul>
					<li>
						<button class="cta">Connect Wallet</button>
					</li>
				</ul>
			</nav>
		</div>
	</header>
</template>

<style scoped>
	header {
		@apply fixed top-0 w-full p-4 z-10;
	}

	header .wrapper {
		@apply flex justify-between items-center p-4 w-full max-w-6xl bg-white m-auto rounded-xl shadow-lg;
	}

	header .logo {
		@apply font-bold text-2xl;
	}
</style>
