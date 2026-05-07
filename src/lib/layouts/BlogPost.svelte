<script lang="ts">
	export let title: string;
	export let author: string;
	export let date: string;
</script>

<article class="space-y-15">
	<header class="space-y-2">
		<h1 class="text-4xl md:text-5xl xl:text-6xl font-bold">
			{title}
		</h1>
		<p class="text-md text-gray-700 dark:text-gray-300">
			By {author} &bull;
			<time datetime={date}>
				{new Date(date).toLocaleDateString('en-GB', { year: 'numeric', month: 'long', day: 'numeric' })}
			</time>
		</p>
	</header>
	
	<div class="prose dark:prose-invert text-xl prose-headings:text-4xl prose-headings:md:text-5xl prose-headings:xl:text-6xl prose-p:text-black dark:prose-p:text-white">
		<slot />
	</div>
</article>