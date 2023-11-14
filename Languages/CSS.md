Everything displayed by CSS is a **box**.

## Extrinsic vs Intrinsic
Extrinsic sizing manually sets sizing of box components:
<main>
	<div>
		<p class="awesome">AWESOME</p>
	</div>
</main>
Intrinsic could be used instead:
<main>
	<div>
		<p class="awesome-int">AWESOME</p>
	</div>
</main>
> [!info]
> Using extrinsic sizing, there is a limit to how much content can be added before the content will overflow outside of the box's bounds.


## Box model
Boxes are made of areas which each do a specific job
![[Pasted image 20231025121631.png]]

## Selection
The selector is the part outside of the curly brackets
```css
.selector {. . .}
```

There are a few basic selectors available:
```css
* {. . .}
section {. . .}
.my-class {. . .}
#my-id {. . .}
[data-type='my-data-type'] {. . .}
```

Selectors can be grouped together to match against multiple elements, separated by commas.
```css
strong,
em,
.my-class,
[lang] {. . .}
```

Pseudo classes use a single colon. They respond to the platform state, such as when an element is hovered.
```css
a:hover {. . .}
p:nth-child(even) {. . .}
```

Pseudo elements are types that rather than focusing on a specific state, such as when an element is hovered, they act as if they are inserting a new element with CSS. These use two colons
```css
.my-class::before {. . .}
```

Descendant combinators work by selecting child elements of the selected element, such as a `<p><strong></strong></p>` where the `<strong>` is the child of the `<p>`.
```css
p strong {. . .}
```

Next sibling will select the element which immediately follows another by using a `+` character in your selector.
```css
.top + {. . .}
```

To add space between stacked elements, use the next sibling combinator only if an element is a next sibling of a child element of `.top`. Otherwise, use `.top * {. . .}` to add margin to all child elements of `.top`

Subsequent-sibling combinator is similar to the next-sibling selector, using a `~`. An element just has to follow another element with the same parent, rather than being the next element with the same parent.

Child combinator allows control over recursion. By using `>`, you limit combinator selector to apply only to direct children.

Example:
```css
.top > * + * {. . .}
```
This will only select direct children of top, selecting all of them, and apply to all next siblings of those selected elements.

Compound selectors allow increased specificity
```css
a.my-class {. . .}
```

## Layout
