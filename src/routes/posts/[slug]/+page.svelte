<script lang="ts">
	import type { PageData } from './$houdini';

	export let data: PageData;

	$: ({ Post } = data);

	$: console.log($Post.data);
</script>

<article class="prose bg-white px-6 max-w-screen-lg">
	{#if $Post.data}
    <h1 class="text-4xl font-bold pt-10">{$Post.data.publication?.post?.title}</h1>

		<div class="">
			{@html $Post.data.publication?.post?.content.html}
		</div>
	{/if}
</article>
