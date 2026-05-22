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
		<div class="mb-12 text-4xl font-medium">SANTiHANS</div>
		<div class="prose">
			<h1 class="mb-3 text-4xl font-semibold text-pretty">A better web starts with privacy.</h1>

			<p class="text-lg font-medium text-pretty">
				Santihans is the company behind <a href="https://scrt.link">scrt.link</a> — a zero-knowledge
				tool for sharing sensitive information. We build for real human needs, not business agendas.
			</p>
			<img class="w-36 rounded-full" src="/images/chris.png" alt="Christophe Schwyzer" />
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
