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

<header class="flex items-center sticky top-0 px-5 py-10 space-x-5 backdrop-blur-sm bg-slate-950/80">
	<h1 class="text-3xl font-semibold text-white">
		Nightbird
	</h1>
</header>

<main class="h-screen">
	<div class="flex justify-center h-[34rem] 2xl:px-14">
		<div class="flex flex-grow max-w-[110rem]">
			<div class="flex flex-col flex-grow space-y-5 pt-32 pl-6 sm:pl-8 md:pl-12 lg:pl-14 xl:pl-14 2xl:pl-0">
				<h1 class="text-4xl md:text-5xl xl:text-6xl font-bold text-white">
					Nightbird Engine
				</h1>
				<p class="text-xl md:text-2xl text-white">
					Nightbird is the first AAAA game engine.
				</p>
				<div class="flex space-x-3">
					<div>
						<a href="https://github.com/NightbirdEngine/Nightbird">
							<button class="cursor-pointer bg-blue-400 rounded-lg px-4 py-2 text-lg text-slate-900 hover:bg-blue-500">
								Check it out on GitHub
							</button>
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>

<footer class="flex justify-center py-5 bg-gray-950">
	<h1 class="text-white">&copy; 2025 Nightbird Engine</h1>
</footer>