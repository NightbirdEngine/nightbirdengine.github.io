<script lang="ts">
	import type { PageData } from './$types';

	export let data: PageData;
	const { content: PostContent, meta } = data;

	const siteUrl = 'https://nightbirdengine.github.io';
</script>

<svelte:head>
	<title>{meta.title} | Nightbird</title>
	{#if meta.description}
		<meta name="description" content={meta.description} />
	{/if}
	
	<meta name="og:title" content="{meta.title} | Nightbird" />
	<meta name="og:type" content="article" />
	{#if meta.description}
		<meta name="og:description" content={meta.description} />
	{/if}
	{#if meta.image}
		<meta name="og:image" content={siteUrl}{meta.image} />
		<meta name="twitter:card" content="summary_large_image" />
	{/if}
</svelte:head>

<PostContent />
