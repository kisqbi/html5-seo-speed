# HTML5 AND SEO RESOURCES


## `<figure>`,`<figcaption>` element 

The  [`<figure>`](https://www.w3.org/TR/2011/WD-html5-author-20110809/the-figure-element.html#the-figure-element)  element  [represents](http://www.w3.org/TR/2011/WD-html5-20110525/rendering.html#represents)  some  [flow content](https://www.w3.org/TR/2011/WD-html5-author-20110809/content-models.html#flow-content), optionally with a caption, that is self-contained and is typically referenced as a single unit from the main flow of the document.

The element can thus be used to annotate illustrations, diagrams, photos, code listings, etc, that are referred to from the main content of the document, but that could, without affecting the flow of the document, be moved away from that primary content, e.g. to the side of the page, to dedicated pages, or to an appendix.

The  `<figcaption>`  element child of the element, if any, represents the caption of the  `<figure>`  element's contents. If there is no child  `<figcaption>`  element, then there is no caption.


### Examples

``` 
<figure>
    <picture>
        <source srcset="images/image-seo-named.webp 1x" media="(min-width: 1200px)" type="image/webp">
        <source srcset="images/image-seo-named.jpg 1x" media="(min-width: 1200px)" type="image/jpeg">
        <source srcset="images/image-seo-named.webp" media="(min-width: 800px)" type="image/webp">
        <source srcset="images/image-seo-named.jpg" media="(min-width: 800px)" type="image/jpeg">
        <source srcset="images/image-seo-named.webp" media="(min-width: 480px)" type="image/webp">
        <source srcset="images/image-seo-named.jpg" media="(min-width: 480px)" type="image/jpeg">
        <img width="1024" height="1024" class="responsive-img" src="images/image-seo-named.jpg" loading="lazy" alt="Alt Text!" sizes="(min-width: 400px) 80vw, 100vw">
    </picture>
    <figcaption class="grey-text text-lighten-1 caption scale-transition scale-out">
		<cite>Jabberwocky</cite> (first verse). Lewis Carroll, 1832-98
	</figcaption>
 </figure>
 ```
 
## `<picture>`,`<source>` element 

The [`<picture>`](https://www.w3.org/TR/2011/WD-html5-author-20110809/the-figure-element.html#the-figure-element)  element gives web developers more flexibility in specifying image resources.

The most common use of the <picture> element will be for art direction in responsive designs. Instead of having one image that is scaled up or down based on the viewport width, multiple images can be designed to more nicely fill the browser viewport.

The <picture> element holds two different tags: one or more  [`<source>`](https://html.spec.whatwg.org/multipage/embedded-content.html#the-source-element)  tags and one  [`<img>`](https://html.spec.whatwg.org/multipage/embedded-content.html#the-img-element)  tag.

The <source> element has the following attributes:

-   srcset (required) - defines the URL of the image to show
-   media - accepts any valid media query that would normally be defined in a CSS
-   sizes - defines a single width descriptor, a single media query with width descriptor, or a comma-delimited list of media queries with a width descriptor
-   type - defines the MIME type

The browser will use the attribute values to load the most appropriate image. **The browser will use the first `<source>` element with a matching hint and ignore any following `<source>` tags.**

The `<img>` element is required as the last child tag of the `<picture>` declaration block. The `<img>` element is used to provide backward compatibility for browsers that do not support the `<picture>` element, or if none of the `<source>` tags matched.

The `<picture>` element works similar to the `<video>` and `<audio>` elements. You set up different sources, and the first source that fits the preferences is the one being used.


### Examples

``` 
<picture>
	<source srcset="images/image-seo-named.webp 1x" media="(min-width: 1200px)" type="image/webp">
	<source srcset="images/image-seo-named.jpg 1x" media="(min-width: 1200px)" type="image/jpeg">
	<source srcset="images/image-seo-named.webp" media="(min-width: 800px)" type="image/webp">
	<source srcset="images/image-seo-named.jpg" media="(min-width: 800px)" type="image/jpeg">
	<source srcset="images/image-seo-named.webp" media="(min-width: 480px)" type="image/webp">
	<source srcset="images/image-seo-named.jpg" media="(min-width: 480px)" type="image/jpeg">
	<img width="1024" height="1024" class="responsive-img" src="images/image-seo-named.jpg" loading="lazy" alt="Alt Text!" sizes="(min-width: 400px) 80vw, 100vw">
 </picture>
 ```
 
