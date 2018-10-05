### Notes


The WP WYSIWYG text editor is very finicky and case-sensitive seemingly. Make sure to only use the 'text' tab instead of the 'visual' one. Switching to the visual one seems to actually hide blocks that are hidden via CSS. Additionally, switching between them seems to take away inline HTML event binding for some reason.


#### WYSIWYG Quirks

```
<button onclick="function()">Show More</button>
```

```
<button>Show More</button>
```

#### Script Tag

Another unfortunate side effect of the editor is that it'll try to insert `<p>` tags everywhere including a `script>` tag. Make sure that there aren't any spaces between function declarations. Potentially, also might need to keep everything left-aligned (not totally tested).

```
function one() {
var a = 'example-class';
$(a).css('background-color', 'red');
var b;
}
function two() {
// do more stuff
}
```