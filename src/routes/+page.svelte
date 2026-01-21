<script lang="ts">
	import { Icon } from '@steeze-ui/svelte-icon';
	import { Tiktok } from '@steeze-ui/simple-icons';
</script>

<main class="flex h-screen w-screen flex-col items-center justify-center bg-[#d7d2cf]">
	<h1 class="text-center text-4xl font-semibold">Lovebound Press</h1>
	<span class="mt-2 text-lg">Coming soon!</span>
	<div class="mt-12 flex h-12 items-center gap-4">
		<a
			href="https://tiktok.com/@loveboundpress"
			target="_blank"
			aria-label="TikTok"
			class="block h-full rounded-md p-2 transition-all hover:bg-black/5"
		>
			<Icon src={Tiktok} />
		</a>
	</div>
</main>
