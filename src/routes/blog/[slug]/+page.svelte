<script lang="ts">
	import type { PageData } from './$types';

	export let data: PageData;
	const { content: PostContent, meta } = data;
</script>

<svelte:head>
	<title>{meta.title}</title>
	{#if meta.description}
		<meta name="description" content={meta.description} />
	{/if}
</svelte:head>

<PostContent />
