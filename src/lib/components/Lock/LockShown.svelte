<script>
	import { fade } from 'svelte/transition';

</script>

<main class='hidden-lock absolute w-screen h-screen flex justify-center font-semibold text-white' transition:fade={{ duration: 500 }}>
	<div class='w-full h-full'>

	</div>
	<div class='w-1/2 flex flex-col items-center justify-between pt-80 p-5'>
		<div class='flex flex-col items-center'>
			<div class='profile w-36 h-36 rounded-full' />
			<h1 class='text-xl font-medium mt-4'>
				Windows 11 User
			</h1>
			<input type='password' class='password rounded-lg  h-8 mt-10 bg-gray-700 bg-opacity-60 px-3 text-sm' placeholder='Password...'>
		</div>
	</div>
	<div class='w-full h-full'>

	</div>
</main>

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
				backdrop-filter: blur(32px);
		}
</style>
