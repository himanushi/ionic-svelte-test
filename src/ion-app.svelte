<svelte:options tag="ion-app" />

<script lang="ts">
	import { defineCustomElements } from "@ionic/core/dist/esm-es5/loader.js";
import "@ionic/core/css/ionic.bundle.css";
import { onMount } from "svelte";
	export let name: string;

onMount(() => {

	if (typeof window !== "undefined") {

defineCustomElements(window);

}
})
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>
