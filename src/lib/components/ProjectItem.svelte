<script lang="ts">
	interface Props {
		label: string;
		image?: string;
		bgColor?: string;
		isTextSection?: boolean;
		textColor?: string;
	}

	let { label, image, bgColor = "#000", isTextSection = false, textColor = "white" }: Props = $props();
</script>

<section class="relative w-full overflow-hidden group" style="background-color: {bgColor};">
	{#if isTextSection}
		<div class="w-full h-[80vh] min-h-[600px] flex flex-col items-center justify-center text-center p-8 select-none">
			<h2 class="font-serif text-5xl md:text-7xl lg:text-8xl mb-12 font-normal tracking-wide text-[#1a1a1a]">L'ATELIER</h2>
			<div class="flex flex-col md:flex-row gap-8 md:gap-16 text-[10px] md:text-[11px] tracking-[0.2em] font-sans text-[#1a1a1a] uppercase font-medium">
				<div class="flex flex-col items-center md:items-end leading-relaxed">
					<span>International Artists</span>
					<span>Consultancy Services</span>
				</div>
				<div class="flex flex-col items-center md:items-start leading-relaxed">
					<span>By Angele Alberti</span>
				</div>
			</div>
		</div>
	{:else if image}
		<!-- Use object-cover and w-full. Height is auto to maintain aspect ratio, but we might want min-height or consistent height? 
		     The screenshot shows images of varying heights but generally filling the screen width. 
		     Let's just use w-full and let height be natural, but ensure it's block to avoid gaps. -->
		<img src={image} alt={label} class="w-full h-auto min-h-[50vh] object-cover block" />
	{:else}
		<div class="w-full h-[80vh]"></div>
	{/if}

	<div class="absolute bottom-8 left-8 bg-white px-3 py-2 z-10">
		<span class="text-[10px] font-bold tracking-widest text-black uppercase block leading-none">
			{label}
		</span>
	</div>
</section>
