# CSS-Snippets
Some useful CSS snippets


**DIV without "class"**

```css
div[foo] {
  color:red;
}

div[bar] {
  font-size:9em;
}
```

```html
<div foo bar>
  Hello world
</div>
```




---

**Style Aria-Current without "class"**

```css
[aria-current] {
  font-weight: bold;
}
```



     <a href="https://github.com/" aria-current="false">GitHub</a>


---

**Style Aria-Current using If Not Statment**

```css
[aria-current]:not([aria-current="false"]) {
  font-weight: bold;
}
```


     <!-----This will NOT be bold---->
     <a href="https://github.com/" aria-current="false">GitHub</a>
     
     <!-----This will be bold---->
     <a href="https://github.com/" aria-current="true">GitHub</a>


---

Pure CSS Link Preview


```css

.link_preview {
	 position: relative;
	 display: inline-block;
	 color: #228475;
}
 .link_preview::before {
	 position: absolute;
	 top: 100%;
	 content: attr(href);
	 opacity: 0;
	 display: block;
	 transition: 0.25s all;
	 height: 0;
	 overflow: hidden;
	 padding: 0.25em 1em;
	 background: #fff;
	 box-shadow: 0 0 3px 0 rgba(0, 0, 0, .3);
	 font-size: 0.7em;
	 color: #555;
}
 .link_preview:hover::before {
	 opacity: 1;
	 display: block;
	 height: auto;
}
```

