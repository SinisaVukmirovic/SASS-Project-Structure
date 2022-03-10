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

#### Partial
##### Partials are a way to split up out code into multiple different files. A file (partial) for variables, utilities, components, layouts...
##### Partials files need to be names with a leading underscore "_variables.scss". This tells SASS compiler not to compile these files into CSS files.
##### To be able to use partial files we need to import them with @import 'variables'. Leading underscore or the .scss extention is not necessary.
<pre><code>
_variables.scss

@import "variables";
</code></pre>