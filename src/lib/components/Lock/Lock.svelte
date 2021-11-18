<script>
	import LockShown from '$lib/components/Lock/LockShown.svelte';

	export let isLockedTimeShown = true;
	import { fly } from 'svelte/transition';
</script>

<main class='flex justify-center font-semibold text-white '>
	{#if !isLockedTimeShown}
		<LockShown />
	{/if}
	{#if isLockedTimeShown}
		<div class='w-full h-full'>

		</div>
		<div class='time-container w-1/2 flex flex-col items-center justify-between pt-40 p-5'
				 transition:fly='{{ y: -200, duration: 1000 }}'>
			<div class='flex flex-col items-center'>
				<p>
					3:15
				</p>
				<p class='text-2xl font-normal mt-2'>
					Tuesday, September 14
				</p>
			</div>
			<div class='font-medium text-sm flex flex-col items-center'>
				<div class='mb-2'>
					Academic Power Hour
				</div>
				<div>
					Tomorrow: 6:00pm - 7:00pm
				</div>
			</div>
		</div>
		<div class='w-full h-full flex items-end justify-end p-4 px-4' transition:fly='{{ y: -200, duration: 1000 }}'>
			<div class='flex gap-3'>
				<button
					class='py-1 px-1 flex items-center justify-center rounded hover:bg-gray-200 hover:bg-opacity-10 transition active:bg-opacity-30'>
					<img src='https://img.icons8.com/fluency-systems-regular/48/000000/wifi--v1.png' class='w-5' />
				</button>
				<button
					class='py-1 px-1 flex items-center justify-center rounded hover:bg-gray-200 hover:bg-opacity-10 transition active:bg-opacity-30'>
					<img src='https://img.icons8.com/fluency-systems-regular/96/000000/full-battery.png' class='w-5' />
				</button>
			</div>
		</div>
	{/if}
</main>

<style>
    main {
        background: url("/graphics/Lock.png") no-repeat;
        background-size: cover;
        filter: brightness(85%) contrast(125%);
    }

    button {
        filter: invert(100%);
    }

		.time-container {
				font-size: 6.3rem;
		}
</style>
