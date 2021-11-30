<script>
	import Lock from '$lib/components/Lock/Lock.svelte';
	import Main from '$lib/components/Main/Main.svelte';
	import { fade } from 'svelte/transition';

	let isLockedTimeShown = true;
	let isLockShown = true;

	function handleKeyboard(e) {
		let keyCode = e.keyCode;
		isLockedTimeShown = false;
		if (keyCode === 40) {
			isLockedTimeShown = true;
		}
	}

</script>

<svelte:window on:keydown={handleKeyboard} />

<Lock {isLockedTimeShown} bind:isLockShown />


