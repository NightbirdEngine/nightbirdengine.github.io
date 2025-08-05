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

<div class="fixed inset-0 -z-10 overflow-hidden bg-slate-900">
	<div
		class="absolute w-[60vw] h-[60vw] bg-gradient-to-r from-purple-600 via-pink-500 to-purple-500 rounded-full blur-3xl animate-pulse-strong"
		style="top: 10%; left: 20%;">
	</div>
</div>

<header class="flex items-center sticky top-0 px-5 py-7 space-x-5 backdrop-blur-md bg-slate-950/70">
	<a href="/" class="text-3xl font-semibold text-white">
		Nightbird
	</a>
	<nav>
		<a href="/news" class="text-xl text-white">News</a>
	</nav>
</header>

<main class="h-screen">
	{@render children?.()}
</main>

<footer class="flex justify-center py-5 bg-gray-950">
	<h1 class="text-white">&copy; 2025 Nightbird Engine</h1>
</footer>