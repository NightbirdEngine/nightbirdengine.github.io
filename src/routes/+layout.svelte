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

<div class="fixed inset-0 -z-10 overflow-hidden pointer-events-none">
	<div
		class="absolute w-[60vw] h-[60vw] bg-linear-to-r from-purple-600 via-pink-500 to-purple-500 rounded-full blur-3xl animate-pulse-strong"
		style="top: 10%; left: 20%;">
	</div>
</div>

<div class="flex flex-col min-h-screen">
	<header class="flex items-center sticky top-0 px-5 py-6 space-x-5 backdrop-blur-lg bg-slate-50/70 dark:bg-slate-950/70">
		<a href="/" class="flex items-center space-x-1 text-3xl font-semibold text-black dark:text-white">
			<img src="/logo-white.svg" alt="Nightbird Logo" class="w-16 h-16 hidden dark:block" />
			<img src="/logo-black.svg" alt="Nightbird Logo" class="w-16 h-16 dark:hidden" />
			<span>Nightbird</span>
		</a>
		<nav>
			<a href="/blog" class="text-xl text-black dark:text-white">Blog</a>
		</nav>
	</header>

	<main class="flex-1 max-w-7xl space-y-15 py-15 lg:py-25 xl:py-35 px-4 sm:px-6 md:px-10">
		{@render children?.()}
	</main>

	<footer class="flex flex-col text-center justify-center py-5 bg-slate-50/70 dark:bg-slate-950/70 text-gray-700 dark:text-gray-400">
			<h1>&copy; 2026 Nightbird Engine. All rights reserved.</h1>
			<h1>Not affiliated with, endorsed by, or associated with Nintendo. Wii U and Nintendo 3DS are trademarks of Nintendo Co., Ltd.</h1>
	</footer>
</div>
