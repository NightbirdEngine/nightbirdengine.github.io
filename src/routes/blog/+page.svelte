<script lang="ts">
	import { posts } from '$lib/posts';
	import BlogCard from '$lib/components/BlogCard.svelte';
</script>

<svelte:head>
	<title>Blog | Nightbird</title>
</svelte:head>

<h1 class="text-4xl md:text-5xl xl:text-6xl font-bold text-black dark:text-white">
	Blog
</h1>

<ul class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-5 gap-y-6">
	{#each posts as post}
		<li>
			<BlogCard {...post} />
		</li>
	{/each}
</ul>
