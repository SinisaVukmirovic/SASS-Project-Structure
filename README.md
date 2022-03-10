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

#### Math
##### We use SASS Math package by @use "sass:math" at the top of the file
<pre><code>
@use "sass:math";

math.div(10, 2);    => 5
math.floor(3.7);    => 3    
math.max(1px, 10px, 15px, 5px);    => 15px    
</code></pre>

#### Map
##### Maps is SASS is like a colection of variables or values in key-value pairs.
<pre><code>
$colors: (
    "primary": $primary,
    "secondary": $secondary,
    "blue": #1919e6,
    "red": #e61919
);

.btn {
    background-color: map-get($colors, "blue");
}
</code></pre>