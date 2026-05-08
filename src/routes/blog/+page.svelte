<script lang="ts">
	import { posts } from '$lib/posts';
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
			<a href="/blog/{post.slug}" class="group block h-54 p-4 border-2 rounded-lg bg-slate-50/30 dark:bg-slate-950/30">
				<p class="text-md text-gray-700 dark:text-gray-300 mb-1">
					By {post.author} &bull;
					<time datetime={post.date}>
						{new Date(post.date).toLocaleDateString('en-US', { year: 'numeric', month: 'long', day: 'numeric' })}
					</time>
				</p>
				<h2 class="text-lg font-semibold">
					{post.title}
				</h2>
				<p>
					{post.description}
				</p>
			</a>
		</li>
	{/each}
</ul>
