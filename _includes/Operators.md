<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Basic arithmetic</td>
<td><code>           +         </code> , <code>           -         </code> , <code>           *         </code> , <code>           /         </code></td>
</tr>
<tr class="even">
<td>Exponentiation</td>
<td><code>           2^3 == 8         </code></td>
</tr>
<tr class="odd">
<td>Division</td>
<td><code>           3/12 == 0.25         </code></td>
</tr>
<tr class="even">
<td>Inverse division</td>
<td><code>           7\3 == 3/7         </code></td>
</tr>
<tr class="odd">
<td>Remainder</td>
<td><code>           x % y         </code> or <code>           rem(x,y)         </code></td>
</tr>
<tr class="even">
<td>Negation</td>
<td><code>           !true == false         </code></td>
</tr>
<tr class="odd">
<td>Equality</td>
<td><code>           a == b         </code></td>
</tr>
<tr class="even">
<td>Equality ( <a href="#" class="tooltip">composite types <span> The default comparison operator compares only memory addresses for composite types. </span></a> )</td>
<td><code>           is(a, b) # done on bit level         </code></td>
</tr>
<tr class="odd">
<td>Inequality</td>
<td><code>           a != b         </code> or <code>           a ≠ b         </code></td>
</tr>
<tr class="even">
<td>Less and larger than</td>
<td><code>           &lt;         </code> and <code>           &gt;         </code></td>
</tr>
<tr class="odd">
<td>Less than or equal to</td>
<td><code>           &lt;=         </code> or <code>           ≤         </code></td>
</tr>
<tr class="even">
<td>Greater than or equal to</td>
<td><code>           &gt;=         </code> or <code>           ≥         </code></td>
</tr>
<tr class="odd">
<td>Element-wise operation</td>
<td><pre><code>          
            [1, 2, 3] .+ [1, 2, 3] == [2, 4, 6][1, 2, 3] .* [1, 2, 3] == [1, 4, 9]
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Not a number</td>
<td><code>           isnan(NaN)         </code> not(!) <code>           NaN == NaN         </code></td>
</tr>
<tr class="odd">
<td>Ternary operator</td>
<td><code>           a == b ? &quot;Equal&quot; : &quot;Not equal&quot;         </code></td>
</tr>
<tr class="even">
<td>Short-circuited AND and OR</td>
<td><code>           a &amp;&amp; b         </code> and <code>           a || b         </code></td>
</tr>
<tr class="odd">
<td>Object equivalence</td>
<td>a === b</td>
</tr>
</tbody>
</table>
