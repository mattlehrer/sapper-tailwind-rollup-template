<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<Nav {segment}/>

<main class="box-border mx-auto p-8 bg-white max-w-4xl relative">
	<slot></slot>
</main>