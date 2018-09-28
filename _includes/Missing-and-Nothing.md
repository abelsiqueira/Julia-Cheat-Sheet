<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Programmers Null</td>
<td><code>           nothing         </code></td>
</tr>
<tr class="even">
<td>Missing Data</td>
<td><code>           missing         </code></td>
</tr>
<tr class="odd">
<td>Not a Number in Float</td>
<td><code>           NaN         </code></td>
</tr>
<tr class="even">
<td>Filter missings</td>
<td><pre><code>          
            skipmissing([1, 2, missing]) == [1,2]
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Replace missings</td>
<td><pre><code>          
            collect((df[:col], 1))
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Check if missing</td>
<td><pre><code>          
            ismissing(x)
            
              not
            
            x == missing
          
        </code></pre></td>
</tr>
</tbody>
</table>
