<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import ProjectItem from "$lib/components/ProjectItem.svelte";
	import CookieBanner from "$lib/components/CookieBanner.svelte";

	const projects = [
		{
			label: "Aman Brand Identity Evolution",
			image: "https://images.unsplash.com/photo-1544967082-d9d25d867d66?q=80&w=2500&auto=format&fit=crop", // Nature/Book vibe
			bgColor: "#a89f91"
		},
		{
			label: "The Puli Brand Identity",
			image: "https://images.unsplash.com/photo-1533090161767-e6ffed986c88?q=80&w=2500&auto=format&fit=crop", // Dark green abstract
			bgColor: "#1a2b25"
		},
		{
			label: "Courchevel 1850 Campaign",
			image: "https://images.unsplash.com/photo-1516713978258-2400e2694389?q=80&w=2500&auto=format&fit=crop", // Snowy mountain/fashion vibe
			bgColor: "#dbe4e9"
		},
		{
			label: "Aman Product Design",
			image: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=2500&auto=format&fit=crop", // Abstract/Glassy
			bgColor: "#2c3e50"
		},
		{
			label: "L'Atelier Brand Identity",
			isTextSection: true,
			bgColor: "#F2EFE9"
		},
		{
			label: "Aman New York Brand Identity",
			image: "https://images.unsplash.com/photo-1590335787039-4467d54942c4?q=80&w=2500&auto=format&fit=crop", // Interior/Tea vibe
			bgColor: "#cbbba0"
		},
		{
			label: "Hu Jing Restaurant Brand Identity",
			image: "https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?q=80&w=2500&auto=format&fit=crop", // Food/Dark Red vibe
			bgColor: "#3e1c1c"
		},
		{
			label: "Aman Brand Campaigns and Merchandise",
			image: "https://images.unsplash.com/photo-1582650756795-9426d0f6531f?q=80&w=2500&auto=format&fit=crop", // Red umbrella/texture
			bgColor: "#8b0000"
		},
		{
			label: "Sophie Green Book Design",
			image: "https://images.unsplash.com/photo-1543002588-bfa74002ed7e?q=80&w=2500&auto=format&fit=crop", // Book/Hands
			bgColor: "#e67e22"
		},
		{
			label: "Village Brand Identity",
			image: "https://images.unsplash.com/photo-1518531933037-91b2f5f229cc?q=80&w=2500&auto=format&fit=crop", // Dark texture/Mossy
			bgColor: "#000000"
		},
		{
			label: "Janu Grill Brand Identity",
			image: "https://images.unsplash.com/photo-1550989460-0adf9ea622e2?q=80&w=2500&auto=format&fit=crop", // Metallic/Texture
			bgColor: "#cd7f32"
		},
		{
			label: "Canyon Point Campaign",
			image: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=2500&auto=format&fit=crop", // Fashion/Shadows
			bgColor: "#95a5a6"
		},
		{
			label: "Iigura Restaurant Brand Identity",
			image: "https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?q=80&w=2500&auto=format&fit=crop", // Table setting
			bgColor: "#dcdde1"
		},
		{
			label: "Aman Restaurant Brand Identities",
			image: "https://images.unsplash.com/photo-1506744038136-46273834b3fb?q=80&w=2500&auto=format&fit=crop", // Landscape
			bgColor: "#27ae60"
		}
	];
</script>

<Header />

<main class="w-full">
	{#each projects as project}
		<ProjectItem 
			label={project.label} 
			image={project.image} 
			bgColor={project.bgColor}
			isTextSection={project.isTextSection}
		/>
	{/each}
</main>

<CookieBanner />

