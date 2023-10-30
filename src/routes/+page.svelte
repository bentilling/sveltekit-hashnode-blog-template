<script lang="ts">
	import type { PageData } from '$houdini/types/src/routes/$houdini';

	export let data: PageData;

	$: ({ AllPosts } = data);
</script>

{#if $AllPosts?.data?.publication?.posts}
	<ul>
		{#each $AllPosts.data.publication.posts.edges as { node: { title, slug, brief, coverImage } }}
			<a href={`/posts/${slug}`}>
				<div class="p-6 bg-white rounded shadow-sm my-4">
					<h2 class="text-xl pb-5 font-semibold">{title}</h2>
					<div class="flex">
						<img class="rounded-lg shadow-lg w-1/2" src={coverImage?.url} alt={title} />
						<p class="m-4 w-1/2">{brief}</p>
					</div>
				</div>
			</a>
		{/each}
	</ul>
{/if}
