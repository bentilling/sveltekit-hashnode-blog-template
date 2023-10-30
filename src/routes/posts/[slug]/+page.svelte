<script lang="ts">
	import type { PageData } from './$houdini';

	export let data: PageData;

	$: ({ Post } = data);
</script>

<article class="bg-white px-6 max-w-screen-lg">
	{#if $Post.data?.publication?.post}
		<h1 class="text-4xl font-bold pt-10">{$Post.data.publication?.post?.title}</h1>

		<div class="prose prose-h2:underline">
			{@html $Post.data.publication?.post?.content.html}
		</div>
	{/if}
</article>
