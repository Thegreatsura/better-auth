<script lang="ts">
import { cn } from "$lib/utils";
import * as FormPrimitive from "formsnap";

type $$Props = FormPrimitive.FieldErrorsProps & {
	errorClasses?: string | undefined | null;
};

let className: $$Props["class"] = undefined;
export { className as class };
export let errorClasses: $$Props["class"] = undefined;
</script>

<FormPrimitive.FieldErrors
	class={cn("text-destructive text-[0.8rem] font-medium", className)}
	{...$$restProps}
	let:errors
	let:fieldErrorsAttrs
	let:errorAttrs
>
	<slot {errors} {fieldErrorsAttrs} {errorAttrs}>
		{#each errors as error}
			<div {...errorAttrs} class={cn(errorClasses)}>{error}</div>
		{/each}
	</slot>
</FormPrimitive.FieldErrors>
