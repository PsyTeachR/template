# Glossary

You can use the `glossary()` function to automatically link to a term in the [psyTeachR glossary](https://psyteachr.github.io/glossary/) or make your own project-specific glossary.

This will create a link to the glossary and include a tooltip with a short definition when you hover over the term. Use the following syntax in inline r: `glossary("word")`. For example, common <a class='glossary' target='_blank' title='The kind of data represented by an object.' href='https://psyteachr.github.io/glossary/d#data-type'>data types</a> are <a class='glossary' target='_blank' title='A data type representing whole numbers.' href='https://psyteachr.github.io/glossary/i#integer'>integer</a>, <a class='glossary' target='_blank' title='A data type representing a real decimal number' href='https://psyteachr.github.io/glossary/d#double'>double</a>, and <a class='glossary' target='_blank' title='A data type representing strings of text.' href='https://psyteachr.github.io/glossary/c#character'>character</a>.

If you need to link to a definition, but are using a different form of the word, add the display version as the second argument (`display`). You can also override the automatic short definition by providing your own in the third argument (`def`). Add the argument `link = FALSE` if you just want the hover definition and not a link to the psyTeachR glossary.


```r
glossary("data type", 
         display = "Data Types", 
         def = "My custom definition of data types", 
         link = FALSE)
```

[1] "<a class='glossary' title='My custom definition of data types'>Data Types</a>"

You can add a glossary table to the end of a chapter with the following code. It creates a table of all terms used in that chapter previous to the `glossary_table()` function. It uses `kableExtra()`, so if you use it in a code chunk, set `results='asis'`.

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r, echo=FALSE, results='asis'}</code></pre>

```r
glossary_table()
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>



|term                                                                                                 |definition                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------|
|[character](https://psyteachr.github.io/glossary/c.html#character){class="glossary" target="_blank"} |A data type representing strings of text.      |
|[data type](https://psyteachr.github.io/glossary/d.html#data-type){class="glossary" target="_blank"} |My custom definition of data types             |
|[double](https://psyteachr.github.io/glossary/d.html#double){class="glossary" target="_blank"}       |A data type representing a real decimal number |
|[integer](https://psyteachr.github.io/glossary/i.html#integer){class="glossary" target="_blank"}     |A data type representing whole numbers.        |



If you want to contribute to the glossary, fork the [github project](https://github.com/PsyTeachR/glossary), add your terms and submit a pull request, or suggest a new term at the [issues page](https://github.com/PsyTeachR/glossary/issues).
