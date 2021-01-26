<script>
	import Slider from "../components/Slider.svelte";

	let photos = [
		{ id: 5, src: 'https://picsum.photos/id/1062/509/339.jpg' },
		{ id: 1, src: 'https://live.staticflickr.com/65535/49755208118_6d7500b64f_b.jpg' },
		{ id: 2, src: 'https://live.staticflickr.com/65535/49756080057_fa2abe581f_h.jpg' },
		{ id: 3, src: 'https://picsum.photos/id/237/509/339.jpg' },
		{ id: 4, src: 'https://picsum.photos/id/659/509/339.jpg' },
	];
</script>

<style>

</style>

<svelte:head>
	<title>Kris Gaisford</title>
</svelte:head>


<Slider {photos}/>

<div class="flex justify-center mb-5">
	<div class="flex justify-center mt-5"><a href="adopt"><button class="red-color hover:bg-red-800 text-white text-3xl p-2">Learn more</button></a></div>
</div>
