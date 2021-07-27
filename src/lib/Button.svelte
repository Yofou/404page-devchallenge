
<a href="/">
    <slot />
</a>

<style>
    a {
        background: var(--dark-grey);
        color: white;
        
        font-size: 14px;
        font-weight: 700;
        letter-spacing: -0.035em;

        text-transform: uppercase;
        text-decoration: none;
        
        padding: 24px 43px;

        align-self: var(--align-self, start);
        justify-self: var(--justify-self, left);
        margin: var(--margin, 0);
    }
</style>