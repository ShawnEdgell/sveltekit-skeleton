<script lang="ts">
	import { AppBar, LightSwitch, getDrawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings } from '@skeletonlabs/skeleton';

	const drawerStore = getDrawerStore();

	const drawerSettings: DrawerSettings = {
		// Property overrides:
		rounded: 'rounded-none'
	};

	function openDrawer() {
		drawerStore.open(drawerSettings);
	}
</script>

<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
	<svelte:fragment slot="lead">
		<button type="button" on:click={openDrawer} aria-label="Open Menu">
			<svg
				class="block sm:hidden w-8 h-8"
				fill="currentColor"
				viewBox="0 0 24 24"
				xmlns="http://www.w3.org/2000/svg"
			>
				<path
					fill-rule="evenodd"
					clip-rule="evenodd"
					d="M4 5h16v2H4V5zm0 6h16v2H4v-2zm0 6h16v2H4v-2z"
				></path>
			</svg>
		</button>
	</svelte:fragment>
	<nav class="hidden sm:flex space-x-6">
		<a href="/" class="hover:text-primary-500" data-sveltekit-preload-data="hover">Home</a>
		<a href="/about" class="hover:text-primary-500" data-sveltekit-preload-data="hover">About</a>
		<a href="/services" class="hover:text-primary-500" data-sveltekit-preload-data="hover"
			>Services</a
		>
		<a href="/contact" class="hover:text-primary-500" data-sveltekit-preload-data="hover">Contact</a
		>
	</nav>
	<svelte:fragment slot="trail">
		<LightSwitch />
	</svelte:fragment>
</AppBar>
