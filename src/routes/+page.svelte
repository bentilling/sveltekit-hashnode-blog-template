<script lang="ts">
	import PostPreview from '$lib/components/PostPreview.svelte';
	import type { PageData } from './$houdini';

	export let data: PageData;

	$: ({ Publication } = data);
</script>


{#if $Publication.data}
	<ul>
		{#each $Publication.data?.publication?.posts?.edges as post}
			<PostPreview coverImageURL={post.node.coverImage.url} title={post.node.title} brief={post.node.brief} slug={post.node.slug}/>
		{/each}
	</ul>
{/if}
