<script>
	export let title;
	export let description;
	export let time;
</script>

<div class="flex flex-col gap-2 items-center md:items-start">
	<h2 class="font-bold text-2xl lg:text-3xl">{title}</h2>
	<p class="leading-5 w-[80%]">{description}</p>
	<p class="text-xl font-normal">{time}</p>
</div>
