# Gamecraft - Testing notes

## Automatic validation

All project files validated successfully the with HTML checker and CSS checker at https://validator.w3.org/nu, aside from caveats documented below:

-   HTML files have information-level alerts about redundant slash in self-closing tags. These are present because the _Prettier_ formatting tool adds the slashes, without an option to turn it off. There is a [long standing issue](https://github.com/prettier/prettier/issues/5246) about this.
-   The CSS validation reports `mask` statements as invalid, such as:  
    ```
    mask: url(../icons/menu.svg) center/cover;
    ```  
    This appears to be a false positive related to `mask` shorthand parsing. The syntax is correct as per the formal definition at [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/mask#formal_syntax), the property validates (and still works the same) when split into 3 individual properties (`mask-image`, `mask-position` and `mask-size`), and the [GitHub issue](https://github.com/w3c/css-validator/issues/151) regarding CSS masking implementation in the validator is open, suggesting that the validator doesn't have full support for it yet.

The Lighthouse report shows a score of 100 in every category:

![Lighthouse report card](lighthouse.png)

## Manual testing

Check the following points to confirm that the website is working as intended:

-   The page opens near-immediately, with no visible and distracting layout jumps,
-   All images and backgrounds load, rather than being missing or displaying a "broken image" icon,
-   The font used for text is as specified in [DESIGN.md](DESIGN.md#design-language) rather than the default sans serif system font,
-   Text never overlaps another part of the layout,
-   Paragraphs are never too wide or too thin to be comfortably read,
-   All text is comfortable to read, with sufficient contrast over the background color/image,
-   Every link and navigation element leads to the specified destination, or displays a "forbidden" cursor when hovered over,
-   Anchor links scroll to the correct section of the page, and the heading is not overlapped by the sticky header,
-   **All** of the points above hold true below the tablet (720px) and mobile (480px) breakpoints, down to the lowest supported width of 300px,
-   Below the 720px breakpoint, the pop-up hamburger menu is always drawn on top of all other content,
-   **All** of the points above hold true on all four pages of the project.

The site was tested to work properly using this procedure in latest Chrome, Firefox and Edge, as well as mobile Chrome.
