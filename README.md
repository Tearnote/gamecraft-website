# Gamecraft: a portfolio website in pure HTML5+CSS3

![Mock-up of the website on desktop, table and mobile screens](doc/mockup.png)

This is a static website for a fictional videogame creation tool called _Gamecraft_, made for [Code Institute](https://codeinstitute.net)'s 1st submission project.

[Live version is available here.](https://tearnote.github.io/gamecraft-website/)

## Notes

The site features both internal and external links. Since Gamecraft doesn't actually exist, the external links are intentionally non-functional, and are only there to make the site look more believable. You can identify these links on desktop by the cursor changing to the "forbidden" sign when you hover over the link.

For the same reason, images of Gamecraft features and example projects are stock images rather than real screenshots.

UX design notes are available in [DESIGN.md](doc/DESIGN.md).

The testing procedures are described in [TESTING.md](doc/TESTING.md).

## Features

![Screenshot of the site header on desktop](doc/header-desktop.png)
![Screenshot of the site header on mobile](doc/header-mobile.png)

Site can be navigated using the sticky header (which collapses into a hamburger menu on smaller screens,) as well as inline links to related content.

![Screenshot of the eye-catch section](doc/eyecatch.png)

The eye-catch section features an attractive scrolling image behind a clear statement of purpose and immediate call to action.

![Screenshot of the features section](doc/features.png)

The features section lists the most important points that distinguish the product from the competition.

![Screenshot of the footer section](doc/footer.png)

The footer section lists all internal and external links and important section anchors together, as well as business details.

![Screenshot of the Asset Store page](doc/asset-store.png)

The Asset Store page showcases thumbnails of some 3D models featured in the product, with a link to access the full store within the product itself.

![Screenshot of the Pricing page](doc/pricing.png)

The Pricing page features a pricing table with clearly defined tiers.

![Screenshot of the contact form on the Support page](doc/support-form.png)

The Support page contains a contact form, with field validation and browser auto-complete support. The form is sent to a "form dump" endpoint.

## Code conventions

The site uses no frameworks, and the only externally loaded resource is Google Fonts. Layout is done with Flexbox. Images are served in the WebP format, with lossy compression set to 90. All code and text files are formatted with [Prettier](https://prettier.io), with indentation using tabs (not spaces.) The CSS is split into sections with `#section` markers, which can be collapsed in most IDEs and code editors.

The compatibility goal was all commonly used desktop and mobile browsers, updated to the latest or second-latest version. In particular, this means no compatibility with IE11, since it is [out of general support](https://learn.microsoft.com/en-us/lifecycle/faq/internet-explorer-microsoft-edge#what-is-the-lifecycle-policy-for-internet-explorer-) since June 15, 2022. The service [Can I use?](https://caniuse.com) was used to ensure that the compatibility goal is met.

## Bugs

A few issues are present in the finished website, they will be documented below.

-   **Form autocomplete doesn't match page style**  
    This is caused by browser-specific styles overriding the CSS when the browser's autocompletion feature is used. The solution would require research for the right CSS vendor prefixes to use to style the form controls during autocomplete, and there wasn't time to look deeper into this during project time. A workaround of setting form controls to "light mode" was applied, which improved text legibility in this situation.
-   **Hamburger menu doesn't have the backdrop blur effect**  
    The area behind the hamburger navigation is not blurred, even though the whole header has the property applied, and the header is a parent of the navigation. This results in a minor decrease to legibility of the navigation on mobile screens in some scenarios. Was not able to find the cause during project time.

## Attribution

All external code snippets are attributed inline.

Stock images:

-   `hero.webp` by [Patricio González](https://pixabay.com/users/patolenin-991181/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=6741424) from [Pixabay](https://pixabay.com//?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=6741424)
-   `feature1.webp` by [Stefano Intintoli](https://unsplash.com/@stefano_intintoli?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `feature2.webp` by [Matthew Kwong](https://unsplash.com/@mattykwong1?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `feature3.webp` by [Wahid Khene](https://unsplash.com/@wahidkhene?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `feature4.webp` by [Ralston Smith](https://unsplash.com/@ralstonhsmith?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `gallery1.webp` by [Raghav Verma](https://unsplash.com/@ragv_v?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `gallery2.webp` by [Pramod Tiwari](https://unsplash.com/@pramodtiwari?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `gallery3.webp` by [Nick Brunner](https://unsplash.com/@nickbrunner?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `gallery4.webp` by [Anita Chong](https://unsplash.com/@jacutanita?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `ball.webp` by [Rodion Kutsaiev](https://www.pexels.com/photo/white-yellow-and-blue-ball-8566875/)
-   `cart.webp` by [emirhan bal](https://pixabay.com/users/7898250-7898250/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=3248226) from [Pixabay](https://pixabay.com//?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=3248226)
-   `cat.webp` by [Andy Hermawan](https://unsplash.com/@kolamdigital?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
-   `hand.webp` by [cottonbro CG studio](https://www.pexels.com/photo/persons-hand-doing-peace-sign-8832763/)

[SVG icons](assets/icons): [CSS.gg](https://css.gg/)
