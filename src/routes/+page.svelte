<script lang="ts">
	import type { PageData } from './$houdini';

	export let data: PageData;
	$: ({ UserDetails } = data);
</script>

<div class="flex h-dvh w-dvw flex-col items-center justify-center">
	<h1 class="text-4xl font-bold">Welcome to SvelteKit {$UserDetails.data?.user.name}!</h1>
	<p class="my-custom-class">
		Visit <a
			href="https://kit.svelte.dev"
			class="font-bold text-orange-600 hover:text-orange-500 hover:underline">kit.svelte.dev</a
		> to read the documentation
	</p>
</div>

<style>
	.my-custom-class {
		margin-top: 2rem;
	}
</style>
