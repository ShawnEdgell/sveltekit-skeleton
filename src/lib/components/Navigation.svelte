<script lang="ts">
	import { getDrawerStore } from '@skeletonlabs/skeleton';

	const drawerStore = getDrawerStore();

	function closeDrawer() {
		drawerStore.close();
	}
</script>

<div class="h-full w-full flex flex-col justify-center items-center space-y-5 p-4">
	<a
		href="/"
		on:click={closeDrawer}
		class="btn btn-lg w-full variant-filled"
		data-sveltekit-preload-data="hover">Home</a
	>
	<a
		href="/about"
		on:click={closeDrawer}
		class="btn btn-lg w-full variant-filled"
		data-sveltekit-preload-data="hover">About</a
	>
	<a
		href="/services"
		on:click={closeDrawer}
		class="btn btn-lg w-full variant-filled"
		data-sveltekit-preload-data="hover">Services</a
	>
	<a
		href="/contact"
		on:click={closeDrawer}
		class="btn btn-lg w-full variant-filled"
		data-sveltekit-preload-data="hover">Contact</a
	>
</div>
