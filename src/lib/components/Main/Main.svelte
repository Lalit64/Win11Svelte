<script>
	import { crossfade } from 'svelte/transition';
	import Start from '$lib/components/Main/Start.svelte';
	import { fadeIn,fadeOut } from '$lib/animations/pageFade';

	let startShown = false;
</script>



<style>
	main {
      background-image: url('/graphics/Background.jpg');
      background-size: cover;
      background-position: center;
	}

	.taskbar {
			backdrop-filter: blur(25px);
	}

  .start-container {
      height: calc(100vh - 2.5rem);
  }
</style>
