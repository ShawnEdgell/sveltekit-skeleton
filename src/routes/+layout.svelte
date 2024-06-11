<script lang="ts">
	import '../app.postcss';
	import { initializeStores, Drawer } from '@skeletonlabs/skeleton';
	import { page } from '$app/stores'; // Importing page store to determine the route

	initializeStores();

	// Highlight JS
	import hljs from 'highlight.js/lib/core';
	import 'highlight.js/styles/github-dark.css';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';
	import xml from 'highlight.js/lib/languages/xml'; // for HTML
	import css from 'highlight.js/lib/languages/css';
	import javascript from 'highlight.js/lib/languages/javascript';
	import typescript from 'highlight.js/lib/languages/typescript';

	hljs.registerLanguage('xml', xml); // for HTML
	hljs.registerLanguage('css', css);
	hljs.registerLanguage('javascript', javascript);
	hljs.registerLanguage('typescript', typescript);
	storeHighlightJs.set(hljs);

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

	// Components
	import AppBar from '$lib/components/AppBar.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Navigation from '$lib/components/Navigation.svelte';
</script>

<Drawer>
	<Navigation />
</Drawer>

<div class="flex flex-col min-h-screen items-center">
	<div class="sticky top-0 z-10 w-full">
		<AppBar />
	</div>
	<div class="flex-grow flex items-center justify-center w-full h-full">
		<slot />
	</div>
</div>
<Footer />
