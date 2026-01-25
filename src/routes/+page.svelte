<script lang="ts">
	import { Icon, type IconSource } from '@steeze-ui/svelte-icon';
	import { Etsy, Instagram, Tiktok } from '@steeze-ui/simple-icons';
</script>

{#snippet link({ href, iconSrc, label }: { href: string; iconSrc: IconSource; label: string })}
	<a
		{href}
		target="_blank"
		class="flex h-12 w-full items-center justify-start gap-4 rounded-md border border-[#ede7d9] bg-[#ede7d9] px-4 py-3 transition-all hover:bg-[#ede7d9]/50"
	>
		<Icon src={iconSrc} class="size-6" />
		{label}
	</a>
{/snippet}

<div class="flex h-screen w-screen flex-col items-center justify-center bg-[#fdf9f0]">
	<main class="flex h-screen max-w-3xl flex-col items-center justify-center gap-12">
		<h1 class="text-center text-4xl font-semibold">Lovebound Press</h1>
		<div class="flex w-full max-w-52 flex-col items-center gap-4">
			{@render link({
				label: '@loveboundpress',
				iconSrc: Tiktok,
				href: 'https://tiktok.com/@loveboundpress'
			})}
			{@render link({
				label: 'LoveboundPress',
				iconSrc: Etsy,
				href: 'https://www.etsy.com/shop/loveboundpress'
			})}
			{@render link({
				label: '@lovebound.press',
				iconSrc: Instagram,
				href: 'https://www.instagram.com/lovebound.press/'
			})}
		</div>
	</main>
</div>
