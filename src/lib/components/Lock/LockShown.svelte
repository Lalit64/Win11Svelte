<script>
	import { fade } from 'svelte/transition';
	let password;
	export let isLockShown = true;
	let hint = false

	function handleKeyboard(e) {
		let keyCode = e.keyCode;
		if (keyCode === 13) {
			if (password === "password") {
				isLockShown = false;
			} else {
				hint = true;
			}
		}
	}

</script>

<svelte:window on:keydown={handleKeyboard}/>

{#if isLockShown}
	<main class='hidden-lock absolute w-screen h-screen flex justify-center font-semibold text-white' transition:fade={{ duration: 500 }}>
		<div class='w-full h-full'>

		</div>
		<div class='w-1/2 flex flex-col items-center justify-between pt-80 p-5'>
			<div class='flex flex-col items-center'>
				<div class='profile w-36 h-36 rounded-full shadow-lg' />
				<h1 class='text-xl font-medium mt-4 '>
					Windows 11 User
				</h1>
				<input type='password' bind:value={password} class='password rounded-lg h-8 mt-10 bg-gray-700 bg-opacity-60 px-3 text-sm transition duration-300 focus:outline-none border-b-2 border-transparent shadow-lg focus:border-blue-600' placeholder='Password...'>
				<p class='text-xs text-red-500 mt-2 flex flex-col  items-center'>
          {#if hint}
            Incorrect password
						<p class='text-gray-200 mt-2'>
	            Hint: password
						</p>
          {/if}
			</div>
		</div>
		<div class='w-full h-full'>

		</div>
	</main>
{/if}


<style>
    main {
        backdrop-filter: blur(25px);
    }

		.profile {
				background-image: url("/graphics/UserLogo.png");
				background-position: center;
				background-size: 90%;
		}

		.password {
				backdrop-filter: blur(25px);
		}

		input :focus{
				outline: none;
		}
</style>
