This was my first project with Frontend Mentor.
See the hosted project [here](https://wrgrant.github.io/fm-minimal-blog-card/).

I have decided to embrace learning frontend development properly by completing the projects focused on basic HTML and CSS.



Things that I learned while implementing this design:

Some nuance about `span` and `div`:
- `span` is inline element, so it doesn't take the full width of the container.
- `div` is block element, so it takes the full width of the container.
- `inline-block` is a combination of both inline and block elements.
- `inline-block` is useful when you want to style a part of a text or an image.

Particularly for the tag component, it makes more sense to use `<span>` than `<div>` since we only want highlighting and style applied to the word. BUT, in order for the tag to have it's own vertical space, we need it to be a block component, so it can be a `<p>`, and we can put the `<span>` inside the `<p>`.

Edit: while tidying up the spacing between elements, I learned that the `margin-top` and `margin-bottom` propeties are ignored by inline elements, such as `<span>`. So I had to change the `display` property of the `<span>` to `inline-block` to get the margin property to work. When I have this `display` property set, I can also just use a `<div>` instead of a `<span>` to wrap the text for the tag. Interesting!


I learned about using the Google Fonts API.
By varying the `font-weight` I can set the "boldness" of the font.
There is a nuance to the Google Fonts API, it is case-sensitive for font names!
So you have to inspect in the browser to make sure that the CSS stylesheet is being loaded correctly.

I learned this the hard was because I was not able to smoothly vary the `font-weight` property. It had big jumps in weight at 400 and 600. I didn't realize that the browser was falling back to a default `sans-serif` font which it only has a few weights for.



I learned about negative margins. These were needed to extend the `<hr>` outside of the `.card` container, so that it reached the outer edges of the `main-container`.

I had to enter a negative margin to counteract the padding on the `.card` container, which puts a margin around the edges of the `.card` container.

I learned about the `line-height` property which is used to set the line spacing of text. 

I learned about the selector syntax of `.class-name > *` which selects all the children of the `.class-name` container. I didn't actually use this for anything, but it will likely be useful for future projects.
