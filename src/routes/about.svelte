<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<div class="content">
	<h1>About Paper View Events</h1>

	<p>
		Paper View Events was founded in 2021 as a way to promote rising Super Smash Brothers stars and cultivate an unprescendented display of sportsmanship.
	</p>

	<p>
		The first two events have focused on the ongoing rival between The Beast and A Baby. So far, A baby has comfortably remained victorious in both events.
	</p>

	<p>
		Please follow Paper View Events on Twitch, and check back on this website for more updates, including stats, videos, and more coming soon.
	</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
