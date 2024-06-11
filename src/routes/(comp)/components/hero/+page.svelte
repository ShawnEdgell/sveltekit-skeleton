<script lang="ts">
	import { CodeBlock } from '@skeletonlabs/skeleton';
</script>

<div class="my-6 p-6 space-y-5">
	<CodeBlock
		language="html"
		code={`<section class="flex items-center justify-center w-full text-center p-6">
	<div>
		<h1 class="text-5xl font-bold mb-4">Welcome to Your Website</h1>
		<p class="text-xl mb-6">This is your hero section, use it to grab attention!</p>
		<a href="/about" class="btn variant-filled-primary" data-sveltekit-preload-data="hover"
			>About Us</a
		>
	</div>
</section>

`}
	></CodeBlock>
</div>
