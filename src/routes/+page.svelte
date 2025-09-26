<script>
	import landingPageContent from '../content/landing.json';
	import Step from '$lib/components/Step.svelte';
	import MatchItem from '$lib/components/MatchItem.svelte';
	import phoneImg from '../lib/assets/goose-iphone-2.png';
	const { hero, steps, matches, phoneImgInfo } = landingPageContent;
</script>

<div class="bg-goose-gradient text-goose-grey-text">
	<!-- Hero Section -->
	<header class="px-5 pt-40 pb-25 flex flex-col gap-5 justify-center items-center text-center">
		<h1 class="font-bold text-3xl md:text-4xl">{@html hero.title}</h1>
		<p class="text-lg md:text-xl leading-6 w-[80%]">{@html hero.subtitle}</p>
	</header>

	<!-- Steps Section -->
	<!-- Step 1 -->
	<section
		class="px-5 md:px-15 lg:px-30 flex flex-col gap-5 md:gap-0 md:flex-row text-center md:text-start justify-between items-center"
	>
		<Step title={steps[0].title} description={steps[0].description} time={steps[0].time} />

		<div class="sm:w-3/5 md:w-2/5 lg:w-1/2 flex justify-center items-center lg:mx-30">
			<img src={phoneImg} alt={phoneImgInfo.alt} />
		</div>
	</section>
</div>

<!-- Step 2 -->
<section
	class="py-40 pl-5 md:pl-15 lg:pl-30 flex flex-col gap-15 md:gap-5 lg:gap-10 xl:gap-30 md:flex-row text-center md:text-start items-center justify-between"
>
	<div class="pr-5 md:pr-0">
		<Step title={steps[1].title} description={steps[1].description} time={steps[1].time} />
	</div>

	<ul class="w-full md:w-[85%] lg:w-2/3 flex flex-col gap-1 overflow-hidden">
		{#each matches as match}
			<MatchItem name={match.name} role={match.role} color={match.color} />
		{/each}
	</ul>
</section>
