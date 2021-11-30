<script>
	import { onMount } from 'svelte';

	let isReady = false;

	onMount(() => {
		isReady = true;
	});
</script>

{#if isReady}
	<!-- Language: Svelte -->
	<slot />
{/if}

<style global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	main {
		@apply w-screen h-screen;
	}

	*::-webkit-scrollbar {
		display: none;
	}

	@font-face {
		font-family: Segoe UI;
		src: url(/fonts/Segoe\ UI.ttf);
	}

	@font-face {
		font-family: Segoe Fluent Icons;
		src: url(/fonts/Segoe\ Fluent\ Icons.ttf);
	}

	* {
		scrollbar-width: none;
		font-family: Segoe UI;
	}

	i {
		font-family: Segoe Fluent Icons;
	}
</style>
