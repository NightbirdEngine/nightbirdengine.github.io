<script lang="ts">
	import type { PageData } from './$types';

	export let data: PageData;
	const { content: PostContent, meta } = data;
</script>

<svelte:head>
	<title>{meta.title} | Nightbird</title>
	{#if meta.description}
		<meta name="description" content={meta.description} />
		<meta name="og:title" content="{meta.title} | Nightbird" />
		<meta name="og:description" content={meta.description} />
		<meta name="og:type" content="article" />
	{/if}
</svelte:head>

<PostContent />
