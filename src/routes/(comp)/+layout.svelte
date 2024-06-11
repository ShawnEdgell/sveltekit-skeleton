<script lang="ts">
	import { page } from '$app/stores';

	$: classesActive = (href: string) =>
		href === $page.url.pathname ? '!variant-filled-primary' : '';
</script>

<div class="flex min-h-screen w-full">
	<!-- Left Sidebar -->
	<div class="hidden sm:block min-w-64 p-6">
		<!-- Content for the left sidebar -->

		<nav class="list-nav">
			<ul>
				<li>
					<a href="/components" class={classesActive('/components')}>
						<span class="flex-auto">Components</span>
					</a>
				</li>
				<li>
					<a href="/components/appbar" class={classesActive('/components/appbar')}>
						<span class="flex-auto">App Bar</span>
					</a>
				</li>
				<li>
					<a href="/components/footer" class={classesActive('/components/footer')}>
						<span class="flex-auto">Footer</span>
					</a>
				</li>
				<li>
					<a href="/components/hero" class={classesActive('/components/hero')}>
						<span class="flex-auto">Hero</span>
					</a>
				</li>

				<!-- Add more navigation links as needed -->
			</ul>
		</nav>
	</div>

	<!-- Main Content Area -->
	<div class="flex-grow flex justify-center">
		<div class="max-w-3xl space-y-5">
			<slot />
		</div>
	</div>

	<!-- Right Sidebar -->
	<div class="min-w-64 hidden lg:block p-6">
		<!-- Content for the right sidebar -->
	</div>
</div>
