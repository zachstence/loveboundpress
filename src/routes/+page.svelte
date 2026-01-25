<script lang="ts">
	import { Icon, type IconSource } from '@steeze-ui/svelte-icon';
	import { Etsy, Pinterest, Tiktok } from '@steeze-ui/simple-icons';
</script>

{#snippet link({
	site,
	href,
	iconSrc,
	label
}: {
	site: string;
	href: string;
	iconSrc: IconSource;
	label: string;
})}
	<a
		{href}
		target="_blank"
		class="flex w-full items-center justify-start gap-4 rounded-md border border-[#ede7d9] bg-[#ede7d9] px-4 py-3 transition-all hover:bg-[#ede7d9]/50"
		aria-label={site}
		title={site}
	>
		<Icon src={iconSrc} class="size-6" />
		{label}
	</a>
{/snippet}

<div
	class="flex h-screen w-screen flex-col items-center justify-center bg-[#fdf9f0] p-4 text-[#4b4b4b]"
>
	<main class="flex h-screen w-full flex-col items-center justify-center gap-12">
		<img src="/logo.svg" alt="Lovebound Press" class="w-full max-w-96" />
		<div class="flex w-full max-w-80 flex-col items-center gap-4 text-base">
			{@render link({
				site: 'Etsy',
				iconSrc: Etsy,
				label: 'LoveboundPress',
				href: 'https://www.etsy.com/shop/LoveboundPress'
			})}
			{@render link({
				site: 'TikTok',
				iconSrc: Tiktok,
				label: '@loveboundpress',
				href: 'https://tiktok.com/@loveboundpress'
			})}
			{@render link({
				site: 'Pinterest',
				iconSrc: Pinterest,
				label: 'LoveboundPress',
				href: 'https://www.pinterest.com/LoveboundPress/'
			})}
			<!-- {@render link({
				label: '@lovebound.press',
				iconSrc: Instagram,
				href: 'https://www.instagram.com/lovebound.press/'
			})} -->
		</div>
	</main>
</div>
