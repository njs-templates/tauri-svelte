<script lang="ts">
	export const ssr = false;
	export const prerender = true;
	export const csr = true;

	import { onMount } from "svelte";
	import { setPath } from "$lib/modules/getPath";
	import NavBar from "$lib/components/NavBar.svelte";
	import "../app.css";

	// Update navbar on load
	onMount(setPath);
</script>

<main>
	<NavBar />
	<slot />
</main>
