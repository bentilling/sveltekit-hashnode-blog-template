<script>
	import '../app.css';
</script>

<div class="flex flex-col bg-gray-200 w-screen">
	<nav class="bg-gray-600 text-white flex justify-between items-center">
		<h1 class=" font-mono text-xl p-6">Awesome blog built with Svelte and Hashnode Headless</h1>
	</nav>
	<div class="mx-auto grow max-w-3xl">
		<slot />
	</div>
</div>
