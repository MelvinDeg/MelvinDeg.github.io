<script>
	import { slide } from "svelte/transition";
	import { quintOut } from "svelte/easing";
	import { is_shared, currentPage } from "$lib/components/stores.js";
	$currentPage = "news";
	$is_shared = false;

	function copyClipboard(id) {
		wait(); //runs in the background

		var copyText = window.location.host + window.location.pathname + "#" + id; //Copy the URL without eventual bookmarks already in the URL, and add a new bookmark.

		navigator.clipboard.writeText(copyText); //Copy to the client's own clipboard.
	}

	async function wait() {
		$is_shared = true;
		//Display time alertBox.
		await new Promise((resolve) => setTimeout(resolve, 2000));
		$is_shared = false;
	}
</script>

<svelte:head>
	<title>News</title>
</svelte:head>

<div class="container w-11/12 lg:w-3/4 text-center mb-40">
	{#if $is_shared}
		<div
			in:slide={{ delay: 250, duration: 1500, easing: quintOut }}
			out:slide={{ delay: 250, duration: 1000, easing: quintOut }}
			class="alert alert-success shadow-lg absolute top-16  w-11/12 lg:w-3/4"
		>
			<div>
				<span>The link is copied to the clipboard</span>
			</div>
		</div>
	{/if}

	<ul class="my-12">
		<li>
		<li><article id="1" class="border-2 rounded-xl border-black">
			<h1 class="font-bold">Suspendisse elit libero</h1>
			<iframe title="video" class="mx-auto mt-10 w-1/2 aspect-video" src="https://player.vimeo.com/video/370874522?h=bd3326f2b6&color=ffffff&title=0&byline=0&portrait=0"  frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>
			<div class="flex px-5 flex-row justify-between bg-base-300">
				<div class="">
					Published: 2 years ago
				</div>

				<div>
					<button class="btn btn-primary" on:click={()=>copyClipboard(1)}>Share</button>
				</div>
			</article>
		</li>
		<li class="mt-5">
			<article id="2" class="border-2 rounded-xl border-black">
				<h1 class="font-bold">
					Lorem ipsum dolor sit amet, consectetur adipiscing.
				</h1>
				<p>
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut
					accumsan quam erat, in hendrerit dolor luctus in. Morbi
					semper magna id massa ullamcorper, a faucibus metus
					porttitor. Proin ultrices posuere nisl, non egestas purus
					vehicula mollis. Aliquam id leo sed metus gravida vulputate
					eget nec ligula. Donec finibus, quam sit amet convallis
					posuere, arcu quam rutrum enim, sed ullamcorper nibh sem sit
					amet nibh. Quisque sapien ipsum, placerat in nisi a,
					interdum tincidunt magna. Nullam aliquam eros id metus
					pellentesque luctus. Donec porttitor eu leo eu scelerisque.
					Aliquam aliquam nunc eu quam consectetur finibus. Vestibulum
					condimentum neque et lacinia lobortis. Integer tempus auctor
					nulla vitae fringilla. Vivamus sit amet ligula aliquet,
					ultrices est vitae, interdum ipsum. Integer posuere diam sit
					amet metus elementum sodales.
				</p>
				<p class="mt-5">
					Lorem ipsum dolor sit amet, consectetur adipiscing elit.
					Morbi viverra dolor id erat aliquam, a mattis dolor
					pulvinar. Etiam feugiat, urna sed gravida egestas, enim
					sapien vestibulum quam, non facilisis purus urna sit amet
					metus. Pellentesque habitant morbi tristique senectus et
					netus et malesuada fames ac turpis egestas. Quisque
					vulputate leo id massa accumsan feugiat. Sed lectus lacus,
					facilisis eleifend felis eu, rhoncus commodo lectus. Nulla
					facilisis, nulla nec luctus venenatis, arcu arcu semper
					massa, vitae iaculis lorem orci non elit. Maecenas vitae
					mauris in nisi aliquam convallis in vel sem. Etiam quis
					massa velit.
				</p>
				<div class="flex px-5 flex-row justify-end bg-base-300">
					<div>
						<button
							class="btn btn-primary"
							on:click={() => copyClipboard(2)}>Share</button
						>
					</div>
				</div>
			</article>
		</li>
		<li class="mt-5">
			<article id="3" class="border-2 rounded-xl border-black">
				<h1 class="font-bold">News from other Sources</h1>
				<ul>
					<li>
						<a
							class="underline decoration-blue-600"
							href="https://www.barncancerfonden.se/barncancerforskning/sa-ska-forskarna-utrota-barncancer/forskningsreportage/hostutlysningen---sophie-degerman/"
							>https://www.barncancerfonden.se/barncancerforskning/sa-ska-forskarna-utrota-barncancer/forskningsreportage/hostutlysningen---sophie-degerman/</a
						>
					</li>
					<li>
						<a
							class="underline decoration-blue-600"
							href="https://www.vk.se/2018-12-21/spannande-att-kunna-paverka-framtidens-vard"
							>https://www.vk.se/2018-12-21/spannande-att-kunna-paverka-framtidens-vard</a
						>
					</li>
				</ul>
				<div class="flex px-5 flex-row justify-end bg-base-300">
					<div>
						<button
							class="btn btn-primary"
							on:click={() => copyClipboard(3)}>Share</button>
					</div>
				</div>
			</article>
		</li>
	</ul>
</div>

<style>
	.container {
		margin-bottom: 75px;
		margin-top: 100px;
	}
</style>
