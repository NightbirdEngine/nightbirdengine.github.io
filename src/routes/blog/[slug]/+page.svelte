<script lang="ts">
	import { page } from '$app/stores';
	import type { PageData } from './$types';

	export let data: PageData;
	const { content: PostContent, meta } = data;

	const siteUrl = 'https://nightbirdengine.github.io';
	$: url = $page.url.href;
</script>

<svelte:head>
	<title>{meta.title} | Nightbird</title>
	{#if meta.description}
		<meta name="description" content={meta.description} />
	{/if}

	<meta name="og:url" content={url} />
	<meta name="og:type" content="article" />
	<meta name="og:title" content="{meta.title} | Nightbird" />

	<meta name="twitter:card" content="summary_large_image">
	<meta property="twitter:domain" content={siteUrl}>
	<meta property="twitter:url" content={url}>
	<meta name="twitter:title" content="{meta.title} | Nightbird">

	{#if meta.description}
		<meta name="og:description" content={meta.description} />
		<meta name="twitter:description" content={meta.description}>
	{/if}
	{#if meta.image}
		<meta name="og:image" content={siteUrl}{meta.image} />
		<meta name="twitter:image" content={siteUrl}{meta.image} />
	{/if}
</svelte:head>

<PostContent />
