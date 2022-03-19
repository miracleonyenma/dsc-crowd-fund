<script setup>
	import { RouterLink, RouterView } from "vue-router";
	import HelloWorld from "@/components/HelloWorld.vue";
	import SiteHeader from "./components/SiteHeader.vue";
</script>

<template>
	<SiteHeader />

	<RouterView />
</template>
