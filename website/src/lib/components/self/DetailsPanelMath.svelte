<script lang="ts">
	import type { CalculatorSearchDetail } from '$lib/types/searchDetails';
	import * as Card from '$lib/components/ui/card';

	let { details } = $props<{ details: CalculatorSearchDetail }>();
</script>

{#if details}
	<Card.Root class="relative w-full bg-card text-card-foreground rounded-xl shadow-custom-inset drop-shadow-md">
		<Card.Header class="pb-3">
			<Card.Title>Calculator</Card.Title>
		</Card.Header>

		<Card.Content class="grid gap-4">
            <div class="flex flex-col gap-4">
                <div class="rounded-md border p-3 hover:bg-primary/10">
                    <p class="text-end font-mono text-md text-muted">{details.expression}=</p>
                    <p class="text-end font-mono text-4xl font-bold">{details.result}</p>
                </div>
            </div>
		</Card.Content>
	</Card.Root>
{/if}