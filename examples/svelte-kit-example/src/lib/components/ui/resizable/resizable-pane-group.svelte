<script lang="ts">
import { cn } from "$lib/utils";
import * as ResizablePrimitive from "paneforge";

type $$Props = ResizablePrimitive.PaneGroupProps;

let className: $$Props["class"] = undefined;
export let direction: $$Props["direction"];
export let paneGroup: $$Props["paneGroup"] = undefined;
export let el: $$Props["el"] = undefined;
export { className as class };
</script>

<ResizablePrimitive.PaneGroup
	bind:el
	bind:paneGroup
	{direction}
	class={cn("flex h-full w-full data-[direction=vertical]:flex-col", className)}
	{...$$restProps}
>
	<slot />
</ResizablePrimitive.PaneGroup>
