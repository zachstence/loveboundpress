<script lang="ts">
	import { Icon, type IconSource } from '@steeze-ui/svelte-icon';
	import { Etsy, Instagram, Tiktok } from '@steeze-ui/simple-icons';
</script>

{#snippet linkIcon({ href, src, label }: { href: string; src: IconSource; label: string })}
	<a
		{href}
		target="_blank"
		aria-label={label}
		class="block h-full rounded-md p-2 transition-all hover:bg-black/5"
	>
		<Icon {src} />
	</a>
{/snippet}

<main class="flex h-screen w-screen flex-col items-center justify-center bg-[#d7d2cf]">
	<h1 class="text-center text-4xl font-semibold">Lovebound Press</h1>
	<span class="mt-2 text-lg">Coming soon!</span>
	<div class="mt-12 flex h-12 items-center gap-4">
		{@render linkIcon({ label: 'TikTok', src: Tiktok, href: 'https://tiktok.com/@loveboundpress' })}
		{@render linkIcon({
			label: 'Etsy',
			src: Etsy,
			href: 'https://www.etsy.com/shop/loveboundpress'
		})}
		{@render linkIcon({
			label: 'Instagram',
			src: Instagram,
			href: 'https://www.instagram.com/lovebound.press/'
		})}
	</div>
</main>
