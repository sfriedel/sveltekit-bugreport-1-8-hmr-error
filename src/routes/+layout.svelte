<script>
	import { FluentProvider } from '@nubolab-ffwd/svelte-fluent';
	import { FluentBundle, FluentResource } from '@fluent/bundle';

	const translations = 'hello = Hello, world!';
	const bundle = new FluentBundle('en');
	bundle.addResource(new FluentResource(translations));
</script>

<FluentProvider bundles={[bundle]}>
	<slot />
</FluentProvider>
