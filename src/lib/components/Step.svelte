<script>
	export let title;
	export let description;
	export let time;
</script>

<div class="flex flex-col gap-3">
	<h2 class="font-bold text-3xl lg:text-4xl">{title}</h2>
	<p class="leading-5">{description}</p>
	<p class="text-2xl font-normal">{time}</p>
</div>
