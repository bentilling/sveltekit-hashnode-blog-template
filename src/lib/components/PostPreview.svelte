<script lang="ts">
	export let title: string;
	export let brief: string;
	export let slug: string;
	export let coverImageURL: string;
</script>

<div class="w-1/2 p-10 shaadow-lg bg-white m-6">
	<a href={`/posts/${slug}`}>
		<h2 class=" text-lg font-medium">{title}</h2>
		<img src={coverImageURL} alt={title} />
		<p>{brief}</p>
	</a>
</div>
