<script>
	import { afterNavigate } from '$app/navigation';
	import { page } from '$app/stores';

	let type = '...';

	afterNavigate((navigation) => {
		type = /** @type {string} */ (navigation.type);
	});
</script>

<h1>{$page.url.searchParams.get('q') ?? '...'}</h1>
<h2>{type}</h2>

<form>
	<input name="q" />
	<button>submit</button>
</form>
