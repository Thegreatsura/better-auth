<script lang="ts">
import { cn } from "$lib/utils";
import type { HTMLAttributes } from "svelte/elements";

type $$Props = HTMLAttributes<HTMLSpanElement> & {
	el?: HTMLSpanElement;
};

export let el: $$Props["el"] = undefined;
export let className: $$Props["class"] = undefined;
export { className as class };
</script>

<span
	bind:this={el}
	role="link"
	aria-disabled="true"
	aria-current="page"
	class={cn("text-foreground font-normal", className)}
	{...$$restProps}
>
	<slot />
</span>
