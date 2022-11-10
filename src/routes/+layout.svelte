<script>
    import '@brainandbones/skeleton/themes/theme-skeleton.css';
    import '@brainandbones/skeleton/styles/all.css';
    import '../app.postcss';

    import { AppShell, AppBar, Divider, GradientHeading, LightSwitch, menu, GreenFall } from '@brainandbones/skeleton';
</script>

<AppShell>
    <!-- Header -->
    <svelte:fragment slot="pageHeader">
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<GradientHeading class="text-5xl" tag="h1" direction="bg-gradient-to-br" from="from-primary-500" to="to-accent-500">
						StartViaUs
					</GradientHeading>
				</a>
			</svelte:fragment>
			<svelte:fragment slot="trail">
					<!-- Navigation -->
		<!-- Links -->
		<!-- prettier-ignore -->
		<section class="hidden lg:flex space-x-6">
			<!-- Docs -->
			<a class="unstyled font-bold" href="/docs/why" data-sveltekit-prefetch>Docs</a>
			<!-- Guides -->
			<a class="unstyled font-bold" href="/guides/install" data-sveltekit-prefetch>Guides</a>
			<!-- Features -->
			<div class="relative">
				<button class="unstyled font-bold space-x-2" use:menu={{ menu: 'features' }}>
					<span>Features</span>
					<span class="opacity-50">▾</span>
				</button>
				<div class="card overflow-hidden w-60 shadow-xl grid grid-cols-1" data-menu="features">
					<!-- Tailwind -->
					<a class="grid grid-cols-[auto_1fr] gap-4 p-4 hover:bg-hover-token" href="/elements/core" data-sveltekit-prefetch>
						<div class="flex justify-center items-center">
						</div>
						<div>
							<h4>Tailwind</h4>
							<small>Elements styled by Tailwind.</small>
						</div>
					</a>
					<hr>
					<!-- Svelte -->
					<a class="grid grid-cols-[auto_1fr] gap-4 p-4 hover:bg-hover-token" href="/actions/clipboard" data-sveltekit-prefetch>
						<div class="flex justify-center items-center">
						</div>
						<div>
							<h4>Svelte</h4>
							<small>Actions and Components.</small>
						</div>
					</a>
					<hr>
					<!-- Utilities -->
					<a class="grid grid-cols-[auto_1fr] gap-4 p-4 hover:bg-hover-token" href="/utilities/codeblocks" data-sveltekit-prefetch>
						<div class="flex justify-center items-center">
						</div>
						<div>
							<h4>Utilities</h4>
							<small>Powerful utility features.</small>
						</div>
					</a>
				</div>
			</div>
		</section>

		<Divider vertical borderWidth="border-l-2 opacity-30" />
				<LightSwitch />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
    <slot />
</AppShell>


