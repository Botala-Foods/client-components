<div class="layout">
    <slot></slot>
</div>

<style>
    .layout {
        --headerTotalHeight: calc(var(--headerHeight) + var(--headerMarginY));
        margin-top: var(--headerTotalHeight);
        padding: var(--layoutPadding);
    }
</style>