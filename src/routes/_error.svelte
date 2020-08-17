<script>
	export let status;
	export let error;

	const dev = process.env.NODE_ENV === 'development';
</script>

<svelte:head>
	<title>{status}</title>
</svelte:head>

<h1 class="mx-auto my-2 text-5xl font-bold sm:text-6xl">{status}</h1>

<p class="mx-auto my-4">{error.message}</p>

{#if dev && error.stack}
<pre>{error.stack}</pre>
{/if}
