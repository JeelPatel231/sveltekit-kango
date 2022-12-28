<script>
	import Logo from '$lib/components/logo.svelte';
</script>

<header class="py-6 font-semibold text-neutral-900 dark:text-neutral print:hidden sm:py-10">
	<nav class="flex items-start justify-between sm:items-center">
		<div class="flex flex-row items-center">
			<!-- Logo/Branding -->
			<Logo />
		</div>
		<!-- Header Links -->
		<ul class="flex list-none flex-col ltr:text-right rtl:text-left sm:flex-row">
			<li class="mb-1 sm:mb-0 ltr:sm:mr-7 ltr:sm:last:mr-0 rtl:sm:ml-7 rtl:sm:last:ml-0">
				<a
					class="decoration-primary-500 hover:underline hover:decoration-2 hover:underline-offset-2"
					href="https://google.com"
					title="Google">Google</a
				>
			</li>
			<li class="mb-1 sm:mb-0 ltr:sm:mr-7 ltr:sm:last:mr-0 rtl:sm:ml-7 rtl:sm:last:ml-0">
				<a
					class="decoration-primary-500 hover:underline hover:decoration-2 hover:underline-offset-2"
					href="https://google.com"
					title="Google">Google</a
				>
			</li>
			<!-- Search button -->
			<li class="ltr:sm:mr-7 ltr:sm:last:mr-0 rtl:sm:ml-7 rtl:sm:last:ml-0">
				<button
					id="search-button"
					class="text-base hover:text-primary-600 dark:hover:text-primary-400"
					title="Search (/)"
				>
					<!-- Search icon -->
				</button>
			</li>
		</ul>
	</nav>
</header>
