<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<style>
	@keyframes pulse-strong {
		0%, 100% {
			opacity: 0.1;
		}
		50% {
			opacity: 0.2;
		}
	}
</style>

<div class="flex flex-col min-h-screen bg-slate-300 dark:bg-slate-900">
	<header class="flex items-center sticky top-0 px-5 py-6 space-x-5 backdrop-blur-lg bg-slate-50/70 dark:bg-slate-950/70">
		<a href="/" class="flex items-center space-x-1 text-3xl font-semibold text-black dark:text-white">
			<img src="/logo-white.svg" alt="Nightbird Logo" class="w-16 h-16 hidden dark:block" />
			<img src="/logo-black.svg" alt="Nightbird Logo" class="w-16 h-16 dark:hidden" />
			<span>Nightbird</span>
		</a>
		<nav>
			<a href="/news" class="text-xl text-black dark:text-white">News</a>
		</nav>
	</header>
	
	<main class="flex-1">
		{@render children?.()}
	</main>
	
	<footer class="flex justify-center py-5 bg-slate-50/70 dark:bg-slate-950/70">
		<h1 class="text-black dark:text-white">&copy; 2025 Nightbird Engine</h1>
	</footer>
</div>