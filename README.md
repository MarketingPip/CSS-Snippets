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
[aria-current]:not([aria-current="false"]) {
  font-weight: bold;
}
```



     <a href="https://github.com/" aria-current="false">GitHub</a>


