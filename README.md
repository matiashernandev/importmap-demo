### Import Maps

Import maps allow you to control the behavior of JavaScript module imports by specifying a mapping between the bare module specifiers used in `import` statements and the actual URLs that should be loaded by the browser.

An import map is defined using a `<script>` tag with a `type` attribute set to `"importmap"`. The content of the `<script>` tag is a JSON object that defines the mapping between module specifiers and URLs.

Here's an example of an import map that maps the module specifier `"confetti"` to a specific URL:

```html
<script type="importmap">
	{
		"imports": {
			"confetti": "https://unpkg.com/canvas-confetti@1.4.0/dist/confetti.module.mjs"
		}
	}
</script>
```

With this import map in place, you can use the import() function to dynamically import the confetti module like this:

`import("confetti").then((module) => module.default());`
