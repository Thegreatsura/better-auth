<script lang="ts">
import { cn } from "$lib/utils";
import type { HTMLAttributes } from "svelte/elements";

type $$Props = HTMLAttributes<HTMLDivElement> & {
	el?: HTMLDivElement;
};

export let el: $$Props["el"] = undefined;
let className: $$Props["class"] = undefined;
export { className as class };
</script>

<div bind:this={el} class={cn("mt-auto flex flex-col gap-2 p-4", className)} {...$$restProps}>
	<slot />
</div>
