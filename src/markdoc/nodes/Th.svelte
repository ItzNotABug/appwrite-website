<script lang="ts">
    import type { HTMLTdAttributes } from 'svelte/elements';

    export let align: HTMLTdAttributes['align'] = undefined;
    export let width: HTMLTdAttributes['width'] = undefined;
</script>

<td
    style:width={width ? `${width}px` : undefined}
    style:min-inline-size={width ? 'unset' : undefined}
    role="columnheader"
    class="web-table-head-col"
    {align}
>
    <span class="text-micro uppercase">
        <slot />
    </span>
</td>
