<div class="card">
    <div class="title">
        <slot name="title"></slot>
    </div>
    <slot></slot>
</div>

<style>
    .card {
        padding: var(--cardPadding);
        background: var(--cardBg);
        box-shadow: var(--cardShadow);
        border: var(--line);
        border-radius: var(--borderRadius);
    }

    .card > *:first-child, .title {
        margin-top: var(--cardFirstChildMarginTop);
    }

    .card > *:last-child {
        margin-bottom: var(--cardLastChildMarginBottom);
    }
</style>
