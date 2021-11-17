<script>
	import {onMount} from "svelte"

	let isReady = false;

	onMount(() => {
		isReady = true;
  });

</script>


{#if isReady}
	<!-- Language: Svelte -->
	<slot>

	</slot>
{/if}


<style global>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

		main {
				@apply w-screen h-screen;
		}
</style>
