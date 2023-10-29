<script>
	import '../app.css';
    import NavBar from '$lib/components/NavBar.svelte';
</script>

<div class="flex flex-row bg-gray-200 w-screen">
	<NavBar />
	<div class="mx-auto grow ">
		<slot />
	</div>
</div>
