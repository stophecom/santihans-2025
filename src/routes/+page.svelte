<script>
	import { page } from '$app/state';

	let appName = 'SANTiHANS';
</script>

<svelte:head>
	<title>Home - {appName}</title>
	<meta property="og:title" content="Home - {appName}" />
	<meta
		name="description"
		content="Santihans is a digital company dedicated to building thoughtful, purpose-driven products for
				the web. "
	/>
	<meta name="keywords" content="digital agency, scrt.link" />

	<meta property="og:url" content={page.url.href} />
	<meta property="og:type" content="website" />
	<meta property="og:image" content="/og-image.png" />
	<meta property="og:image:type" content="image/png" />
	<meta property="og:image:width" content="1200" />
	<meta property="og:image:height" content="630" />
	<meta property="og:image:alt" content="Santihans" />
</svelte:head>

<div class="container mx-auto px-4 py-16">
	<main>
		<img src="/logo.svg" alt="Logo" class="mb-12 w-44" />
		<div class="prose">
			<h1 class="mb-3 text-4xl font-semibold text-pretty">
				Building a better web, where privacy and people come first.
			</h1>

			<p class="text-lg font-medium text-pretty">
				Santihans is a digital company dedicated to building thoughtful, purpose-driven products for
				the web. Our current focus is <a href="https://scrt.link">scrt.link</a>, a privacy-conscious
				platform to share sensitive information in the most secure way possible. At the core of
				everything we do is a clear set of values: putting people and privacy before profit, and
				building tools that serve real human needs—not just business agendas.
			</p>
		</div>
	</main>
	<footer class="mt-6 border-t py-4">
		<p>
			SANTiHANS GmbH<br />
			UID: CHE-244.875.499<br />
			CH-4056 Basel
		</p>
		<a href="mailto:info@santihans.com">info@santihans.com</a>
	</footer>
</div>
