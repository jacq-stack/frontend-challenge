<script>
	import landingPageContent from '../content/landing.json';
	import phoneImg from '../lib/assets/goose-iphone.png';
	import phoneImg2 from '../lib/assets/goose-iphone-2.png';
	const { hero, steps, matches, phoneImgInfo } = landingPageContent;
</script>

<div class="bg-goose-gradient text-goose-grey-text">
	<!-- Hero Section -->
	<section class="px-5 pt-40 mb-25 flex justify-center text-center">
		<div>
			<h1 class="font-bold text-4xl md:text-5xl mb-5">{@html hero.title}</h1>
			<p class="text-lg md:text-2xl leading-7">{@html hero.subtitle}</p>
		</div>
	</section>

	<!-- Step 1: 3rd try with flex and cropped-sized iphone-->
	<section
		class="px-5 md:px-15 lg:px-30 flex flex-col md:flex-row text-center md:text-start justify-between items-center"
	>
		<div class="flex flex-col gap-3 mb-5 md:mb-0">
			<h2 class="font-bold text-3xl lg:text-4xl">{steps[0].title}</h2>
			<p class="leading-5">{steps[0].description}</p>
			<p class="text-2xl font-normal">{steps[0].time}</p>
		</div>
		<div class="sm:w-3/5 md:w-2/5 lg:w-1/2 flex justify-center items-center lg:mx-30">
			<img src={phoneImg2} alt={phoneImgInfo.alt} class="" />
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
<section class="flex gap-5 pl-30 py-20">
	<div>
		<h2>{steps[1].title}</h2>
		<p>{steps[1].description}</p>
		<p>{steps[1].time}</p>
	</div>
	<ul>
		{#each matches as match}
			<li>
				<p>{match.name}</p>
				<p>{match.role}</p>
			</li>
		{/each}
	</ul>
</section>

<!-- <section class="bg-goose-gradient px-30 py-35">
	<div>
		<h1>How Goose Delivers Results. Fast.</h1>
		<p>A smarter, simpler way to hire and get hired. Built on efficiency, fairness, and trust</p>
	</div>
	<div>
		<div>
			<h2>Create a Brief</h2>
			<p>Tell us what you need–skills, timeline, budget.</p>
			<p>🕐 ~5 minutes</p>
		</div>
		<img alt="Goose Freelance App" />
	</div>
</section>

<section>
	<div>
		<h2>Get Recommended Matches</h2>
		<p>Our AI surfaces vetted freelancers from trusted referrals.</p>
		<p>🕐 ~1 minute</p>
	</div>
	<ul>
		<li>
			<p>Clara Moreau</p>
			<p>Content Editor & Copywriter</p>
		</li>
		<li>
			<p>Daniel Weber</p>
			<p>Full-Stack Developer & Data Consultant</p>
		</li>
		<li>
			<p>Elena Rossi</p>
			<p>Art Director & Brand Designer</p>
		</li>
		<li>
			<p>Mateo Silva</p>
			<p>Videographer & Motion Editor</p>
		</li>
		<li>
			<p>Anna Novak</p>
			<p>Performance Coach & Workshop Facilitator</p>
		</li>
	</ul>
</section> -->
