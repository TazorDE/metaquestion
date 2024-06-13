<!-- YOU CAN DELETE EVERYTHING IN THIS PAGE -->
<script lang="ts">
	import { page } from '$app/stores';
	import { i18n } from '$lib/i18n';
	import * as m from '$lib/paraglide/messages.js';
	import { availableLanguageTags, languageTag } from '$lib/paraglide/runtime.js';
</script>

<svelte:head>
	<title>{m.title()}</title>
	<meta name="description" content={m.abstract()} />
	<meta name="robots" content="index, follow" />
	<meta
		name="keywords"
		content="questions, meta questions, bad questions, metafrage, smart questions, faq"
	/>
</svelte:head>

<div
	class="container h-full mx-auto flex flex-col justify-center items-center space-y-4 pl-6 pr-4 my-4"
>
	<div class="space-y-5">
		<h1 class="h1">{m.title()}</h1>
		<p>
			{m.abstract()}
		</p>
		<p>
			{m.explanation()}
		</p>
		<h2 class="h2">{m.benefits()}</h2>
		<ul class="list-disc">
			<li>{m.benefit_1()}</li>
			<li>{m.benefit_2()}</li>
		</ul>
		<h2 class="h2">{m.Disadvantages()}</h2>
		<ul class="list-disc">
			<li>
				{m.disadvantage_1()}
			</li>
			<li>
				{m.disadvantage_2()}
			</li>
			<li>
				{m.disadvantage_3()}
			</li>
			<li>
				{m.disadvantage_4()}
			</li>
		</ul>
		<h2 class="h2">{m.examples()}</h2>
		<ul class="list-disc">
			<li>{m.example_1()}</li>
			<li>{m.example_2()}</li>
			<li>{m.example_3()}</li>
			<li>{m.example_4()}</li>
			<li>{m.example_5()}</li>
			<li>{m.example_6()}"</li>
			<li>{m.example_7()}</li>
			<li>{m.example_8()}</li>
		</ul>
	</div>
	<hr class="w-full" />
	<div class="space-y-1 flex flex-col text-center">
		<a
			class="anchor"
			href="http://www.catb.org/~esr/faqs/smart-questions.html"
			target="_blank"
			rel="noopener noreferrer"
		>
			How To Ask Questions The Smart Way
		</a>
		<a class="anchor" href="https://metafrage.de/" target="_blank" rel="noopener noreferrer">
			Based on metafrage.de (German)
		</a>
		<p>{m.languages()}:</p>
		<div class="flex divide-x gap-2 items-center justify-center">
			{#each availableLanguageTags as lang}
				<!-- the hreflang attribute decides which language the link points to -->
				<a
					href={i18n.route($page.url.pathname)}
					class="anchor pl-2"
					hreflang={lang}
					aria-current={lang === languageTag() ? 'page' : undefined}
				>
					{lang}
				</a>
			{/each}
		</div>
		<p class="text-surface-600-300-token">
			Contribute new translations here: <a
				href="https://github.com/TazorDE/metaquestion"
				class="anchor"
				target="_blank"
				rel="noopener noreferrer"
			>
				GitHub
			</a>
		</p>
	</div>
</div>
