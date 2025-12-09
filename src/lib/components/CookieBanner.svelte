<script lang="ts">
	let visible = $state(true);

	function close() {
		visible = false;
	}
</script>

{#if visible}
	<div class="fixed bottom-8 left-8 z-50 bg-white p-5 pr-8 max-w-xs shadow-none border border-gray-100/10">
		<p class="text-[11px] text-black mb-4 font-sans leading-relaxed tracking-wide">
			We use cookies to improve your browsing experience.
		</p>
		<div class="flex gap-6">
			<button onclick={close} class="text-[10px] font-bold tracking-widest uppercase text-gray-400 hover:text-gray-600 transition-colors">
				Decline
			</button>
			<button onclick={close} class="text-[10px] font-bold tracking-widest uppercase text-black hover:opacity-70 transition-opacity">
				Accept
			</button>
		</div>
	</div>
{/if}
