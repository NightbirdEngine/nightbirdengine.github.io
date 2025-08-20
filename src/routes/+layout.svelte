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

  .animate-pulse-strong {
    animation: pulse-strong 5s ease-in-out infinite;
  }
</style>

<div class="fixed inset-0 -z-20 bg-slate-300 dark:bg-slate-900">
	<div
		class="absolute w-[60vw] h-[60vw] bg-gradient-to-r from-purple-600 via-pink-500 to-purple-500 rounded-full blur-3xl animate-pulse-strong"
		style="top: 10%; left: 20%;">
	</div>
</div>

<div class="flex flex-col min-h-[100dvh]">
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