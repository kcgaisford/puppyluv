<script>
	
	// SLIDY START
	import Slidy from 'svelte-slidy'
	
	export let photos;
	
	const slidy_default = {
		slides: photos,
		wrap: {
			id: 'slidy',
			width: '100%',
			// height: '45vw',
			padding: '0',
			align: 'middle',
			alignmargin: 0,
		},
		slide: {
			gap: 10,
			width: '75%',
			height: '100%',
			backimg: false,
			imgsrckey: 'src',
			objectfit: 'cover',
			overflow: 'visable'
		},
		controls: {
			dots: true,
			dotspure: true,
			dotsarrow: true,
			arrows: true,
			keys: true,
			drag: true,
			wheel: false,
		},
	}
	let index = 1
	// SLIDY END

</script>

<style>
	/* :global(#slidy span) {
		left: 50%;
		transform: translateX(-50%)
	} */
	@media screen and (min-width: 900px) {
		:global(#slidy .slidy-ul li) {
			height: 35vw;
			width: 50%;
		}
	}
	@media screen and (max-width: 425px) {
		:global(#slidy .slidy-ul li) {
			height: 60vw;
			width: 75%;
		}
	}
</style>

<Slidy {...slidy_default} bind:index let:item />