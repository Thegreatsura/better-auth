<script lang="ts">
import { AlertDialog as AlertDialogPrimitive } from "bits-ui";
import { cn } from "$lib/utils.js";
import { buttonVariants } from "../button";

type $$Props = AlertDialogPrimitive.CancelProps;
type $$Events = AlertDialogPrimitive.CancelEvents;

let className: $$Props["class"] = undefined;
export { className as class };
</script>

<AlertDialogPrimitive.Cancel
	class={cn(buttonVariants({ variant: "outline" }), "mt-2 sm:mt-0", className)}
	{...$$restProps}
	on:click
	on:keydown
	let:builder
>
	<slot {builder} />
</AlertDialogPrimitive.Cancel>
