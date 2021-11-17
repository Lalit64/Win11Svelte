<script>
	import Lock from '$lib/components/Lock/Lock.svelte';

	let isLockedTimeShown = true;

	function handleUpClick(e) {
		let keyCode = e.keyCode;
		if (keyCode === 38) {
			isLockedTimeShown = false;
		}
		if (keyCode === 40) {
			isLockedTimeShown = true;
		}
  }

</script>

<svelte:window on:keydown={handleUpClick}/>

<Lock {isLockedTimeShown} />
