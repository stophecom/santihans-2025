<script>
	import { page } from '$app/state';

	let appName = 'SANTiHANS';

	const products = [
		{
			name: 'scrt.link',
			url: 'https://scrt.link',
			image: '/images/scrt-link.png',
			tagline: 'Share sensitive information. End-to-end encrypted, one time.'
		},
		{
			name: 'Ponzi Potato',
			url: 'https://www.ponzipotato.com',
			image: '/images/ponzi-potato.webp',
			tagline: 'Plant one potato, build an empire. A free incremental browser game.'
		}
	];
</script>

<svelte:head>
	<title>Home - {appName}</title>
	<meta property="og:title" content="Home - {appName}" />
	<meta
		name="description"
		content="SANTiHANS GmbH is an independent studio from Basel, Switzerland, building and running scrt.link and Ponzi Potato."
	/>
	<meta name="keywords" content="santihans, scrt.link, ponzi potato" />

	<meta property="og:url" content={page.url.href} />
	<meta property="og:type" content="website" />
	<meta property="og:image" content="/og-image.png" />
	<meta property="og:image:type" content="image/png" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />
	<meta property="og:image:alt" content="SANTiHANS GmbH" />
</svelte:head>

<div class="container mx-auto max-w-3xl px-4 py-16">
	<main>
		<div class="mb-12 text-4xl font-medium">SANTiHANS</div>

		<h1 class="mb-4 text-4xl font-semibold text-pretty">Products people love to use.</h1>
		<p class="mb-12 text-lg text-pretty text-gray-700">
			SANTiHANS GmbH is an independent studio from Basel, Switzerland. We believe a better web
			starts with privacy and fun.
		</p>

		<ul class="mb-16 grid gap-6 sm:grid-cols-2">
			{#each products as product (product.url)}
				<li>
					<a
						href={product.url}
						class="group block overflow-hidden border border-gray-300 transition hover:border-gray-500"
					>
						<img
							class="aspect-[1200/630] w-full object-cover"
							src={product.image}
							alt={product.name}
							width="1200"
							height="630"
						/>
						<div class="p-4">
							<div class="flex items-baseline justify-between text-xl font-medium">
								<span class="group-hover:underline">{product.name}</span>
								<span aria-hidden="true">↗</span>
							</div>
							<p class="mt-1 text-gray-600">{product.tagline}</p>
						</div>
					</a>
				</li>
			{/each}
		</ul>

		<div class="prose">
			<img class="w-24 rounded-full" src="/images/chris.png" alt="Christophe Schwyzer" />
			<div>
				Christophe Schwyzer - Founder<br />
				Contact: <a href="https://www.linkedin.com/in/stophecom/">LinkedIn</a> |
				<a href="https://bsky.app/profile/stophe.com">Bluesky</a> |
				<a href="https://stophe.com">Web</a>
			</div>
		</div>
	</main>
	<footer class="prose mt-6 border-t border-gray-300 py-4">
		SANTiHANS GmbH<br />
		UID:
		<a href="https://www.zefix.admin.ch/en/search/entity/list/firm/1316279">CHE-244.875.499</a><br
		/>
		CH-4056 Basel<br />

		Email: <a href="mailto:info@santihans.com">info@santihans.com</a>

		<div class="mt-5 border-t border-gray-300 py-4">
			<small class="text-gray-700"
				>©{new Date().getFullYear()} SANTiHANS GmbH - Made in Switzerland</small
			>
		</div>
	</footer>
</div>
