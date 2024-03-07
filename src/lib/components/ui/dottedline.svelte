<script lang="ts">
  export let line: "large" | "small";
  import ArrowUp from "$lib/components/icons/arrowup.svelte";
  let heights = {
    large: {
      lineHeight: 250,
      circle: 4,
    },
    small: {
      lineHeight: 150,
      circle: 8,
    },
  };
  let h = heights[line].lineHeight;
  let circle = heights[line].circle;
</script>

<div class=" w-2 flex flex-col items-center gap-1">
  <div class="flex flex-col items-center">
    {#if line !== "large"}
      <ArrowUp />
    {/if}
    <div
      class="h-[{h / 2}px] border-l-4 w-0 border-dotted border-slate-300"
    ></div>
  </div>
  <div
    class="w-{circle} h-{circle} border-{circle} rounded-full border-[#0066FF]"
  ></div>
  <div
    class="h-[{h / 2}px] border-l-4 w-0 border-dotted border-slate-300"
  ></div>
</div>
