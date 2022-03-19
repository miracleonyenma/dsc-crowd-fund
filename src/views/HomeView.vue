<script setup>
	import { ref } from "vue";
	import TheWelcome from "@/components/TheWelcome.vue";
	import RequestForm from "../components/RequestForm.vue";

	const showForm = ref(false);
</script>

<template>
	<main>
		<section class="overflow-hidden">
			<div class="wrapper flex flex-col-reverse md:flex-row items-center py-24 min-h-[24rem]">
				<header>
					<div class="wrapper w-full max-w-3xl">
						<h1 class="font-black text-6xl mb-2">Be a part of something hooge!</h1>
						<p class="text-xl mb-2">Move the community foward through funding. Your contributions matter</p>
						<button @click="showForm = true" class="cta">Create a request</button>
					</div>
				</header>
				<div class="media-cont">
					<div class="img-cont floating-img max-w-2xl">
						<img src="@/assets/img/cryptocurrency-wallet.png" class="object-contain" alt="" />
					</div>
				</div>
			</div>
		</section>

		<div @click.self="showForm = false" class="form-modal" :class="{ 'modal-active': showForm }">
			<RequestForm class="request-form" :class="{ 'form-active': showForm }" />
		</div>
	</main>
</template>

<style scoped>
	.form-modal {
		@apply fixed top-0 left-0 right-0 bottom-0 flex justify-center opacity-0 invisible p-4 bg-slate-900 bg-opacity-60 z-20;
	}

	.form-modal.modal-active {
		@apply visible opacity-100;
	}

	.form-modal .request-form {
		@apply absolute bottom-0 transition-all duration-300 ease-in-out max-h-0;
	}

	.request-form.form-active {
		@apply max-h-full;
	}
</style>
