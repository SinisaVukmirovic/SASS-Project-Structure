## SASS Project Structure

#### To achieve project structure with CSS and SCSS folders where .scss files in SCSS folder are compiled into .css files in CSS folder, by using Live Sass Compiler VS code extension (by Glenn Marks), we need to setup compilation path in the extension's settings.json file, by adding:
<pre><code>
"liveSassCompile.settings.formats":[
    {
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "~/../css"
    }
]
</code></pre>