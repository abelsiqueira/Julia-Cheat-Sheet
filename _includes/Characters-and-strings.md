<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Character</td>
<td><code>           chr = 'C'         </code></td>
</tr>
<tr class="even">
<td>String</td>
<td><code>           str = &quot;A string&quot;         </code></td>
</tr>
<tr class="odd">
<td>Character code</td>
<td><code>           Int('J') == 74         </code></td>
</tr>
<tr class="even">
<td>Character from code</td>
<td><code>           Char(74) == 'J'         </code></td>
</tr>
<tr class="odd">
<td>Any <a href="https://docs.julialang.org/en/latest/manual/unicode-input">UTF</a> character</td>
<td><pre><code>          
            chr = &#39;\uXXXX&#39;     # 4-digit HEXchr = &#39;\uXXXXXXXX&#39; # 8-digit HEX
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Loop through characters</td>
<td><pre><code>          
            for c in strprintln(c)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Concatenation</td>
<td><code>           str = &quot;Learn&quot; * &quot; &quot; * &quot;Julia&quot;         </code></td>
</tr>
<tr class="even">
<td>String interpolation</td>
<td><pre><code>          
            a = b = 2println(&quot;a * b = $(a*b)&quot;)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>First matching character or regular expression</td>
<td><code>           findfirst(isequal('i'), &quot;Julia&quot;) == 4         </code></td>
</tr>
<tr class="even">
<td>Replace substring or regular expression</td>
<td><code>           replace(&quot;Julia&quot;, &quot;a&quot; =&gt; &quot;us&quot;) == &quot;Julius&quot;         </code></td>
</tr>
<tr class="odd">
<td>Last index (of collection)</td>
<td><code>           lastindex(&quot;Hello&quot;) == 5         </code></td>
</tr>
<tr class="even">
<td>Number of characters</td>
<td><code>           length(&quot;Hello&quot;) == 5         </code></td>
</tr>
<tr class="odd">
<td>Regular expression</td>
<td><code>           pattern = r&quot;l[aeiou]&quot;         </code></td>
</tr>
<tr class="even">
<td>Subexpressions</td>
<td><pre><code>          
            str = &quot;+1 234 567 890&quot;pat = r&quot;\+([0-9]) ([0-9]+)&quot;m = match(pat, str)m.captures == [&quot;1&quot;, &quot;234&quot;]
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>All occurrences</td>
<td><code>           [m.match for m = eachmatch(pat, str)]         </code></td>
</tr>
<tr class="even">
<td>All occurrences (as <a href="https://slendermeans.org/julia-iterators.html">iterator</a> )</td>
<td><code>           eachmatch(pat, str)         </code></td>
</tr>
</tbody>
</table>

Beware of multi-byte Unicode encodings in UTF-8:

<div class="centred">

``` 
    
      10 == lastindex("Ångström") != length("Ångström") == 8
    
  
```

</div>

Strings are immutable.
