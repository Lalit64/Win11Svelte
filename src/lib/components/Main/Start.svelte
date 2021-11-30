<script>
	import {fly} from "svelte/transition";
	import SearchIcon from "@fluentui/svg-icons/icons/search_20_filled.svg";
	import ChevronRight from "@fluentui/svg-icons/icons/chevron_right_20_regular.svg"
	import Icon from '$lib/components/Main/Icon.svelte';
</script>

<div class='start w-1/4 h-1/2 rounded-lg bg-gray-900 bg-opacity-60 bottom-14 flex flex-col' transition:fly={{ y: 1000, duration: 300 }}>
	<div class='bg-gray-800 rounded border-blue-600 border-b-4 flex shadow-lg m-5'>
		<Icon src={SearchIcon} customStyles='mx-3 w-5' />
		<input type='text' placeholder='Type here to search' class='w-full py-2 bg-transparent text-white transition duration-300 focus:outline-none  '>
	</div>
	<div class='h-full m-5'>
		<div class='font-bold p-5 text-white flex justify-between items-center'>
			Pinned
			<button class='bg-gray-700 p-0.5 px-3 rounded text-xs flex items-center justify-center bg-opacity-50'>
				All Apps <Icon src={ChevronRight}  />
			</button>
		</div>
	</div>
	<div class='h-full m-5'>
		<div class='font-bold text-sm p-5 text-white flex justify-between items-center'>
			Recommended
		</div>
	</div>
	<div class='h-36 bg-black bg-opacity-20 rounded-b-lg p-3 flex items-center justify-between px-16 text-white'>
		<div class='flex items-center'>
			<div class='user-profile w-10 h-10 rounded-full mr-2'></div>
			Windows 11 User
		</div>

	</div>
</div>

<style>

	.start {
			backdrop-filter: blur(40px);
	}

	.user-profile {
      background-image: url("/graphics/UserLogo.png");
      background-position: center;
      background-size: 90%;
	}
</style>
