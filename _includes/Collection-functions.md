<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Apply <code>           f         </code> to all elements of collection <code>           coll         </code></td>
<td><code>           map(f, coll)         </code> or
<pre><code>          
            map(coll) do elem# do stuff with elem# must contain returnend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Filter <code>           coll         </code> for true values of <code>           f         </code></td>
<td><code>           filter(f, coll)         </code></td>
</tr>
<tr class="odd">
<td>List comprehension</td>
<td><code>           arr = [f(elem) for elem in coll]         </code></td>
</tr>
</tbody>
</table>
