<script>
	export let segment;
</script>

<style>
	nav {
		background-color: #3c3c3c;
		color: white;
		border-bottom: 1px solid rgb(182, 28, 28);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		align-self: flex-end;
		float: left;
		bottom:0;
		padding: 0 0.5em;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 4px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 0.5em 0.4em;
		display: block;
	}
</style>

<nav class="shadow-xl">
	<ul class="flex justify-center">
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">HOME PAGE</a></li>
		<li><a aria-current="{segment === 'about' ? 'page' : undefined}" href="about">ABOUT US</a></li>
		<!-- Logo Middle of Nav -->
		<li><a href="." class="text-3xl sm:text-4xl font-bold -mb-4">PUPPY LUV</a></li>
		<!-- End Logo Middle of Nav -->
		<li><a rel=prefetch aria-current="{segment === 'adopt' ? 'page' : undefined}" href="adopt">ADOPT ME</a></li>
		<li><a rel=prefetch aria-current="{segment === 'portfolio' ? 'page' : undefined}" href="blog">OUR DOGS</a></li>
	</ul>
	<div class="flex justify-center mb-1 sm:mb-3">Find Your Best Friend</div>
</nav>

