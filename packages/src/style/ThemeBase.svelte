<slot></slot>

<style>
    :global(:root) {
         /* Define Colors as colors */
        --neonGreen: #C5F3C1;
        --brown: #D2B48C;
        --lightBrown: #FEF6E4;
        --peach: #F3D2C1;
        --red: #CF5048;
        --neonPink: #F582AE;
        --black: #001858;
        --darkBlue: #172C66;
        --blue: #5E84BC;
        --neonBlue: #8BD3DD;
        --gray: #BCB8C8;
        --lightGray: #D9D7E0;

        /* Define Colors intentions */
        --primary: var(--blue);
        --danger: var(--red);
        --background: var(--lightBrown);
        --textColor: var(--black);
        --textAccentColor: var(--darkBlue);
        --buttonColor: var(--primary);
        --buttonTextColor: var(--background);
        --lineColor: var(--black);
        --cardBg: var(--background);
        --headerBackground: var(--background);
        --headerLinkColor: var(--textAccentColor);
        --footerTextColor: var(--textAccentColor);
        --footerBackground: var(--brown);

        /* Spacing scale */
        --s-1: .25rem;  /* 4px */
        --s-2: .5rem;   /* 8px */
        --s-3: .75rem;  /* 12px */
        --s-4: 1rem;    /* 16px */
        --s-5: 1.25rem; /* 20px */
        --s-6: 1.5rem;  /* 24px */
        --s-8: 2rem;    /* 32px */
        --s-10: 2.5rem; /* 40px */
        --s-12: 3rem;   /* 48px */
        --s-16: 4rem;   /* 64px */
        --s-20: 5rem;   /* 80px */

        /* Elevation */
        --level-1: 3px 3px 0px rgba(0, 24, 88, 0.16);
        --level-2: 5px 5px 0px rgba(0, 24, 88, 0.13);
        --level-3: 6px 6px 0px rgba(0, 24, 88, 0.1);
        --level-n1: inset 4px 5px 0px rgba(0, 24, 88, 0.2);
        --level-n2: inset 6px 7px 0px rgba(0, 24, 88, 0.13);

        /* Lines */
        --lineThin: solid calc(.5 * var(--s-1)) var(--lineColor);
        --line: solid calc(.75 * var(--s-1)) var(--lineColor);

        /* Type */
        --headingFont: "Dillan", sans-serif;
        --lineHeight: 1.65;
        --bodyFont: "Work Sans", sans-serif;
        --baseFontSize: 16px;
        --h1: 3.157rem;
        --h2: 2.369rem;
        --h3: 1.777rem;
        --h4: 1.333rem;
        --h5: 1rem;
        --smallText: 0.75rem;

        /* Padding and margin */
        --layoutPadding: var(--containerPadding);
        --headerMarginX: var(--s-2);
        --headerMarginY: var(--s-2);
        --footerPadding: 2rem var(--containerPadding);
        --containerPadding: 2.5%;
        --cardPadding: var(--s-8);
        --buttonPadding: var(--s-2) var(--s-10);
        --buttonPaddingSmall: var(--s-2) var(--s-5);
        --cardFirstChildMarginTop: 0; /* First item will never have margin top */
        --cardLastChildMarginBottom: 0; /* Last item will never have margin bottom */
        
        /* Height and width */
        --headerHeight: var(--s-12);
        --buttonHeight: inherit;
        --buttonWidth: inherit;
        
        /* Borders */
        --borderRadius: var(--s-1);
        --buttonBorderRadius: var(--borderRadius);

        /* Shadows */
        --headerShadow: var(--level-2);
        --blockquoteShadow: var(--level-3);
        --buttonShadow: var(--level-1);
        --buttonShadowHover: var(--level-2);
        --cardShadow: var(--level-2);
    }
</style>