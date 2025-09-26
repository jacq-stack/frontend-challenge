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

	<!-- Step 1: 3rd try with flex and cropped-sized iphone-->
	<section
		class="px-5 md:px-15 lg:px-30 flex flex-col gap-5 md:gap-0 md:flex-row text-center md:text-start justify-between items-center"
	>
		<!-- <div class="flex flex-col gap-3">
			<h2 class="font-bold text-3xl lg:text-4xl">{steps[0].title}</h2>
			<p class="leading-5">{steps[0].description}</p>
			<p class="text-2xl font-normal">{steps[0].time}</p>
		</div> -->
		<Step title={steps[0].title} description={steps[0].description} time={steps[0].time} />

		<div class="sm:w-3/5 md:w-2/5 lg:w-1/2 flex justify-center items-center lg:mx-30">
			<img src={phoneImg} alt={phoneImgInfo.alt} class="" />
		</div>
	</section>
</div>

<!-- Steps Section -->
<!-- Step 1: first try -->
<!-- <section class="flex gap-5 bg-goose-gradient text-goose-grey-text px-30">
	<div class="">
		<h2 class="font-bold text-3xl md:text-4xl mb-3">{steps[0].title}</h2>
		<p>{steps[0].description}</p>
		<p>{steps[0].time}</p>
	</div>
	<div class="flex">
		<img src={phoneImg} alt={phoneImgInfo.alt} class="max-w-2/3" />
	</div>
</section> -->

<!-- Step 1: 2nd try with Grid and full-sized iphone-->
<!-- <section
	class="md:grid md:grid-cols-10 md:items-center bg-goose-gradient text-goose-grey-text px-5 md:px-15 lg:px-30"
>
	<div class="col-span-3 flex flex-col gap-3">
		<h2 class="font-bold text-3xl md:text-4xl">{steps[0].title}</h2>
		<p class="leading-5">{steps[0].description}</p>
		<p class="text-2xl font-normal">{steps[0].time}</p>
	</div>
	<div class="col-start-5 col-span-5 h-100 md:h-120 lg:h-180 overflow-hidden">
		<img src={phoneImg} alt={phoneImgInfo.alt} class="p-10 md:pd-0" />
	</div>
</section> -->

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

	<!-- <ul class="w-full md:w-[85%] lg:w-2/3 flex flex-col gap-1 overflow-hidden">
		{#each matches as match}
			<li class="flex items-center">
				<p
					class="text-xs sm:text-sm lg:text-base font-medium px-2 py-1 sm:px-4 sm:py-2 border-1 rounded-full whitespace-nowrap text-center"
				>
					{match.name}
				</p>
				<div
					class="min-w-[10vw] sm:min-w-[15vw] md:min-w-[3vw] ld:min-w-[5vw] h-0.25 bg-text-white"
				></div>
				<p
					class="text-xs sm:text-sm lg:text-base px-1 sm:px-3 py-0.5 border-1 rounded-full whitespace-nowrap text-center text-{match.color}"
				>
					{match.role}
				</p>
				<div class="w-screen h-0.25 bg-text-white"></div>
			</li>
		{/each}
	</ul> -->
</section>
