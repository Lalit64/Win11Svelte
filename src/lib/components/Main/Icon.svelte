<script>
	export let src;
	export let customStyles;
</script>

<object data={src} class={customStyles} >

</object>

<style>
	object {
		filter: invert();
  }
</style>
