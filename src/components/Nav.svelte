<script>
	export let segment;
</script>

<style>
	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255, 62, 0);
		display: block;
		bottom: -1px;
	}
</style>

<nav class="px-4 py-0 font-light border-orange-600 border-solid border-b-1">
	<ul class="clearfix p-0 m-0">
		<li class="block float-left">
			<a
				class="block px-2 py-4 no-underline"
				aria-current="{segment === undefined ? 'page' : undefined}"
				href="."
				>home</a
			>
		</li>
		<li class="block float-left">
			<a
				class="block px-2 py-4 no-underline"
				aria-current="{segment === 'about' ? 'page' : undefined}"
				href="about"
				>about</a
			>
		</li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<li class="block float-left">
			<a
				class="block px-2 py-4 no-underline"
				rel="prefetch"
				aria-current="{segment === 'blog' ? 'page' : undefined}"
				href="blog"
				>blog</a
			>
		</li>
	</ul>
</nav>
