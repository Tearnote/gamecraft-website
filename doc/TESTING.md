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

## Functional testing

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
-   **All** of the points above hold true on all four pages of the project,
-   The form on the Support page requires filling in all fields, has autocomplete for name and email fields, and submits every field to the form dump endpoint.

The site was tested to work properly using this procedure in latest Chrome, Firefox and Edge, as well as mobile Chrome.

## User stories study

In the design phase, we [established](DESIGN.md#user-stories) the expected user-base and what kinds of questions they might have when visiting the website. We will check if their questions are answered by the finished project.

| Question                                                         | Answered? | How?                                                                                    |
|------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------------------|
| Can I make a videogame in this?                                  | Yes       | Answered in the eye-catch                                                               |
| Is it going to be as confusing as the others?                    | Yes       | Addressed by the first feature                                                          |
| Do I need to make my own graphics and sounds?                    | Yes       | Answered by the projects section, as well as the Asset Store page                       |
| How much does it cost?                                           | Yes       | Answered in the download section, further detailed in Pricing page                      |
| If I finish my game, can I sell it?                              | Yes       | Same as above                                                                           |
| What do I do if I'm stuck with a problem?                        | Yes       | Answered in the download section, further detailed in Support page                      |
| How do I get started? Should I follow any tutorial alongside it? | Yes       | Answered by the second feature                                                          |
| Is this a serious product?                                       | Yes       | Suggested by attractive page design, as well as high quality images in projects section |
| Can you make something complex and professional looking in this? | Yes       | Answered by the projects section                                                        |
| Why would I want to switch from my current workflow to this?     | Yes       | Answered in the third feature                                                           |
| Do I get timely support if I encounter a bug?                    | Yes       | Support options and timeframe detailed on the Support page                              |
| Where can I go in-depth on specific features?                    | Yes       | Options detailed on the Support page                                                    |
