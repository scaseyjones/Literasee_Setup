# What is Markdown?

[Markdown](https://daringfireball.net/projects/markdown/syntax#list) is a simple, lightweight syntax designed by [Jon Gruber](https://en.wikipedia.org/wiki/John_Gruber)
and [Aaron Schwartz](https://en.wikipedia.org/wiki/Aaron_Swartz) to enable the creation of easy-to-read and easy-to-write
text that can be converted to HTML for web-based rendering.

Markdown supports numerous types of content/text formatting including:

* [Headers](#headers)
* [Text](#text)
* [Lists](#lists)
* [Tables](#tables)
* [Blockquotes](#blockquotes)
* [Code & syntax highlighting](#code-syntax-highlighting)
* [Horizontal rules](#horizontal-rules)
* [Hypertext links](#hypertext-links)
* [Embedding graphics](#embedding-graphics)
  - [Embedding bitmap graphics](#embedding-bitmap-graphics)
  - [Embedding vector graphics](#embedding-vector-graphics)
  - [Embedding D3 visualizations](#embedding-d3-visualizations)
  - [Embedding Tableau visualizations](#embedding-tableau-visualizations)
  - [Embedding Plotly visualizations](#embedding-plotly-visualizations)
* [Embedding videos](#embedding-videos)


---

## Headers

Headers (except for H1) in Literasee support deep-linking via [AnchorJS](http://bryanbraun.github.io/anchorjs/)

```
# H1 Heading
## H2 Heading
### H3 Heading
#### H4 Heading
##### H5 Heading
###### H6 Heading
```

# H1 Heading

## H2 Heading

### H3 Heading

#### H4 Heading

##### H5 Heading

###### H6 Heading

---


## Text

```
**Bold** or __Bold__
_Italic_ or *Italic*
_**Bold Italic**_ or **_Bold Italic_**
~~strike through~~
```

**Bold** or __Bold__

_Italic_ or *Italic*

_**Bold Italic**_ or **_Bold Italic_**

~~strike through~~

---


## Lists

```
1. First ordered list item
2. Another item
  * Unordered sub-list.
  - Second item of unordered sub-list using minus.
  + Third item of unordered sub-list using plus.
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
  2. Second item of sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.
   Note that this line is separate, but within the same paragraph.
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)
```

1. First ordered list item
2. Another item
  * Unordered sub-list.
  - Second item of unordered sub-list using minus.
  + Third item of unordered sub-list using plus.
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
    2. Second item of sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
   Note that this line is separate, but within the same paragraph.⋅⋅
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

---

## Tables

You can create tables by assembling a list of words and dividing them with hyphens - (for the first row),
and then separating each column with a pipe |:

```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell


To enhance readability, you can also add extra pipes on the ends:

```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Note that the dashes at the top don't need to match the length of the header text exactly. Text emphasis is also supported in tables.

```
| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |
| Email     | Initiate email window |
| ~~Twitter~~   | ~~Tweet~~ |
```

| Name | Description          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |
| Email     | Initiate email window |
| ~~Twitter~~   | ~~Tweet~~ |

---

## Blockquotes

```
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

---


## Code & syntax highlighting


```js
if (isAwesome){
  return true
}
```


```R
x <- rnorm(100, mean=50, sd=10)
y <- x + rnorm(100)
plot(x, y)
```

---

## Horizontal rules

```
Three or more...

---

Hyphens

***

Asterisks

___

Underscores
```

Three or more...

---

Hyphens

***

Asterisks

___

Underscores


---

## Hypertext links

```
| Markdown | Result |
|----------|--------|
| `[An inline-style link](http://literasee.io)` | [An inline-style link](http://literasee.io)|
| `[An inline-style link with title](http://literasee.io "Literasee Homepage")` | [An inline-style link with title](http://literasee.io "Literasee Homepage") |
| `[A reference-style link][Arbitrary case-insensitive reference text]` | [A reference-style link][Arbitrary case-insensitive reference text] |
| `[A numbered reference-style link][1]` | [A numbered reference-style link][1] |
| `[A relative reference to a repository file](../blob/master/LICENSE)` | [A relative reference to a repository file](../blob/master/LICENSE) |

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com> and sometimes
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.nciea.org
[1]: http://www.nciea.org
```

| Markdown | Result |
|----------|--------|
| `[An inline-style link](http://literasee.io)` | [An inline-style link](http://literasee.io)|
| `[An inline-style link with title](http://literasee.io "Literasee Homepage")` | [An inline-style link with title](http://literasee.io "Literasee Homepage") |
| `[A reference-style link][Arbitrary case-insensitive reference text]` | [A reference-style link][Arbitrary case-insensitive reference text] |
| `[A numbered reference-style link][1]` | [A numbered reference-style link][1] |
| `[A relative reference to a repository file](../blob/master/LICENSE)` | [A relative reference to a repository file](../blob/master/LICENSE) |

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com> and sometimes
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.nciea.org
[1]: http://www.nciea.org

---


## Embedding graphics

Because Literasee is web-based, it can embed a variety of graphics/images/visualizations.

### Embedding bitmap graphics

Literasee logo embedded inline and reference (hover to see the title text):

```
Inline-style:
![alt text](https://avatars0.githubusercontent.com/u/16685371?v=3&s=200 "Literasee logo")

Reference-style:
![alt text][logo]

[logo]: https://avatars0.githubusercontent.com/u/16685371?v=3&s=200 "Literasee logo"
```

Inline-style:
![alt text](https://avatars0.githubusercontent.com/u/16685371?v=3&s=200 "Literasee logo")

Reference-style:
![alt text][logo]

[logo]: https://avatars0.githubusercontent.com/u/16685371?v=3&s=200 "Literasee logo"


---

### Embedding vector graphics

```
<a href="https://literasee.github.io">
    <img src="https://literasee.github.io/public/Literasee_symbol_right_trimmed.svg"
    style="width: 100%;">
</a>
```

<a href="https://literasee.github.io"><img src="https://literasee.github.io/public/Literasee_symbol_right_trimmed.svg" style="width: 100%;"></a>


---

### Embedding D3 visualizations

```
<iframe
    width="100%"
    height="510"
    scrolling="no"
    src="https://rawgit.com/bclinkinbeard/0192cf1c32d6fc50d247/raw/689619eeefdb0d79c1d0cbca935ca677c13cdfce/index.html">
</iframe>
```

<iframe
    width="100%"
    height="510"
    scrolling="no" src="https://rawgit.com/bclinkinbeard/0192cf1c32d6fc50d247/raw/689619eeefdb0d79c1d0cbca935ca677c13cdfce/index.html">
</iframe>


---

### Embedding Tableau visualizations

```
<iframe
    src="https://public.tableau.com/views/50YearsofCrime/USCrimeDashboard?:embed=y&:loadOrderID=0&:display_count=yes&:showTabs=y"
    width="800"
    height="800">
</iframe>
```

<iframe
    src="https://public.tableau.com/views/50YearsofCrime/USCrimeDashboard?:embed=y&:loadOrderID=0&:display_count=yes&:showTabs=y"
    width="800"
    height="800">
</iframe>


---

### Embedding Plotly visualizations

```
<iframe
    src="https://plot.ly/~matlab_user_guide/1963.embed?width=640&height=480."
    width="800"
    height="600">
</iframe>
```

<iframe
    src="https://plot.ly/~matlab_user_guide/1963.embed?width=800&height=600."
    width="800"
    height="600">
</iframe>

---

## Embedding videos

Markdown doesn't directly support the inclusion of videos. However, Markdown
supports HTML which can be used to embed videos:

```
<iframe
    style=“border: 2px solid #111111;”
    src="https://player.vimeo.com/video/62604492?color=c9ff23&byline=0&portrait=0"
    width="800"
    height="450"
    frameborder="0"
    webkitallowfullscreen mozallowfullscreen allowfullscreen>
</iframe>
```

<iframe src="https://player.vimeo.com/video/62604492" width="640" height="360" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
