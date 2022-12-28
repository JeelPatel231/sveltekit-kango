<script lang="ts">
	import Logo from '$lib/components/logo.svelte';

	const linkMap : {[key:string] : string } = {
		'Docs' : 'docs',
		'Samples' : 'samples',
		'Users' : 'users',
		'GitHub' : 'https://github.com/AvinashReddy3108/literate-fortnight'
	}
</script>

<header class="py-6 font-semibold text-neutral-900 dark:text-neutral print:hidden sm:py-10">
	<nav class="flex items-start justify-between sm:items-center">
		<div class="flex flex-row items-center">
			<!-- Logo/Branding -->
			<Logo />
		</div>
		<!-- Header Links -->
		<ul class="flex list-none sm:gap-8 flex-col ltr:text-right rtl:text-left sm:flex-row">
			{#each Object.entries(linkMap) as [label, link]}
				<li class="mb-1 sm:mb-0 ltr:sm:mr-7 ltr:sm:last:mr-0 rtl:sm:ml-7 rtl:sm:last:ml-0">
					<a
						class="decoration-primary-500 hover:underline hover:decoration-2 hover:underline-offset-2"
						href={link}
						title={label}>{label}</a
					>
				</li>
			{/each}
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
