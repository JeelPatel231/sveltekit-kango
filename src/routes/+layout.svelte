<script>
	import '../app.postcss';
	import Header from '$lib/components/header/basic.svelte';
	import Footer from '$lib/components/footer.svelte';
</script>

<div id="the-top" class="absolute flex self-center">
	<a
		class="px-3 py-1 text-sm -translate-y-8 rounded-b-lg bg-primary-200 focus:translate-y-0 dark:bg-neutral-600"
		href="#main-content"
		><span class="font-bold text-primary-600 ltr:pr-2 rtl:pl-2 dark:text-primary-400">&darr;</span
		>Skip to main content</a
	>
</div>

<Header />

<div class="relative flex flex-col grow">
	<main id="main-content" class="grow">
		<slot />
		<div class="pointer-events-none absolute top-[100vh] bottom-0 w-12 ltr:right-0 rtl:left-0">
			<a
				href="#the-top"
				class="pointer-events-auto sticky top-[calc(100vh-5.5rem)] flex h-12 w-12 items-center justify-center rounded-full bg-neutral/50 text-xl text-neutral-700 backdrop-blur hover:text-primary-600 dark:bg-neutral-800/50 dark:text-neutral dark:hover:text-primary-400"
				aria-label="Scroll to top"
				title="Scroll to top"
			>
				&uarr;
			</a>
		</div>
	</main>
	<Footer />
</div>
