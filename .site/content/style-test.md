+++
title = "Style Test"
author = ["James"]
date = 2025-12-10T00:00:00+00:00
draft = false
+++

This page demonstrates all org-mode syntax elements and how they're rendered in the published site.


## Headings {#headings}


### Level 2 Heading {#level-2-heading}


#### Level 3 Heading {#level-3-heading}

<!--list-separator-->

-  Level 4 Heading

    <!--list-separator-->

    -  Level 5 Heading


## Text Formatting {#text-formatting}

Regular paragraph text with **bold**, _italic_, <span class="underline">underline</span>, ~~strikethrough~~, and `highlighted text` (verbatim).

You can also use `code snippets` inline like this.


## Lists {#lists}


### Unordered Lists {#unordered-lists}

-   First item
-   Second item
    -   Nested item 1
    -   Nested item 2
        -   Deep nested item
-   Third item
-   Fourth item with longer text to see how wrapping works in the design


### Ordered Lists {#ordered-lists}

1.  First numbered item
2.  Second numbered item
    1.  Nested numbered
    2.  Another nested
3.  Third item


### Mixed Lists {#mixed-lists}

-   Bullet point
    1.  Numbered sub-item
    2.  Another numbered
-   Another bullet
    -   Nested bullet
        1.  Deep numbered


## Links {#links}


### Internal Links {#internal-links}

Link to another note:

Link to heading in same file:


### External Links {#external-links}

Visit for documentation.


## Code Blocks {#code-blocks}


### Inline Code {#inline-code}

Use `git status` to check repository state.


### Code Block {#code-block}

```python
def fibonacci(n):
    """Calculate fibonacci number recursively."""
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

# Test it
print(fibonacci(10))
```


### Another Language {#another-language}

```elisp
(defun my-function (arg)
  "Example Emacs Lisp function."
  (message "Hello %s!" arg))

(my-function "World")
```


## Tables {#tables}


### Simple Table {#simple-table}

| Name    | Age | City     |
|---------|-----|----------|
| Alice   | 30  | New York |
| Bob     | 25  | London   |
| Charlie | 35  | Tokyo    |
| Diana   | 28  | Paris    |


### Table with Alignment {#table-with-alignment}

| Left aligned | Center | Right |
|--------------|:------:|------:|
| Text         | 123    | 4.56  |
| More text    | 789    | 10.11 |


### Longer Table {#longer-table}

| Number | Name    | Age | Gender | City     |
|--------|---------|-----|--------|----------|
| 1      | Alice   | 30  | Female | New York |
| 2      | Bob     | 25  | Male   | London   |
| 3      | Charlie | 35  | Male   | Tokyo    |
| 4      | Diana   | 28  | Female | Paris    |


## Quotes {#quotes}

> This is a blockquote. It can span multiple lines and is used for citing text or emphasizing important passages.
>
> It supports multiple paragraphs as well.


## Special Blocks {#special-blocks}


### Example Block {#example-block}

```text
This is an example block.
  It preserves formatting.
    Including indentation.
```


### Verse Block {#verse-block}

<div class="verse">

Roses are red<br />
Violets are blue<br />
Org mode is great<br />
And so are you<br />

</div>


## Emphasis and Highlighting {#emphasis-and-highlighting}

-   This has `highlighted text` which should be prominent
-   This has `inline code` which is different
-   This is **bold** and this is _italic_
-   This is <span class="underline">underlined</span> and this is ~~strikethrough~~


## Images {#images}

Example image link (if it exists):

-   ::


## Horizontal Rule {#horizontal-rule}

Above the line.

---

Below the line.


## Definition Lists {#definition-lists}

Term 1
: Definition of term 1

Term 2
: Definition of term 2 with more details

Long Term
: This is a longer definition that might wrap to multiple lines to demonstrate how definition lists are rendered


## Checkboxes {#checkboxes}

-   [ ] Unchecked item
-   [-] Partially checked item
-   [X] Checked item
-   [ ] Another unchecked with longer text to see wrapping behavior


## Foot notes {#foot-notes}

This text has a footnote reference[^fn:1].

Here's another reference[^fn:2].


## Backlinks Test {#backlinks-test}

This note should show backlinks from any note that links to it. Try creating a link to this test page from another note to see how backlinks appear at the bottom.


## Summary Section {#summary-section}

This page demonstrates all major org-mode syntax elements. Use it to test:

1.  Typography and heading styles
2.  List formatting
3.  Table rendering
4.  Code block styling
5.  Link behavior
6.  Special blocks and quotes
7.  Text emphasis and highlighting
8.  Backlinks functionality

Check the rendered HTML to ensure everything displays correctly with the org-mode inspired styling.

[^fn:1]: This is the first footnote.
[^fn:2]: This is a named footnote with more details.
