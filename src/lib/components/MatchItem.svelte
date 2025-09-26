<script>
	export let name;
	export let role;
	export let color;

	// Color mapping
	const colorMap = {
		orange: '#e8a56c',
		purple: '#8448a7',
		green: '#488b81',
		yellow: '#d1e299',
		blue: '#527a9a'
	};

	$: colorValue = colorMap[color] || '#ffffff';
	$: textStyle = `color: ${colorValue};`;
	$: borderStyle = `border-color: ${colorValue};`;
	$: gradientStyle = `background: linear-gradient(to right, #ffffff, ${colorValue});`;
	$: gradientStyle2 = `background: linear-gradient(to right, ${colorValue} 80%, #ffffff) 20%;`;
</script>

<li class="flex items-center">
	<!-- Name badge -->
	<div class="flex-shrink-0">
		<p
			class="text-xs sm:text-sm lg:text-base font-medium px-2 py-1 sm:px-4 sm:py-2 border rounded-full whitespace-nowrap text-center"
		>
			{name}
		</p>
	</div>

	<!-- Connecting line  -->
	<div class="flex-shrink-0 w-8 sm:w-12 md:w-16 h-px" style={gradientStyle}></div>

	<!-- Role badge with color -->
	<div class="flex-shrink-0">
		<p
			class="text-xs sm:text-sm lg:text-base font-medium px-2 py-1 sm:px-3 sm:py-1 border rounded-full whitespace-nowrap text-center"
			style="{textStyle} {borderStyle}"
		>
			{role}
		</p>
	</div>

	<!-- Connecting line  -->
	<div class="flex-grow min-w-4 h-px" style={gradientStyle2}></div>
</li>
