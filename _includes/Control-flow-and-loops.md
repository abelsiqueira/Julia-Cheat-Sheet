<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Conditional</td>
<td><code>           if         </code> - <code>           elseif         </code> - <code>           else         </code> - <code>           end         </code></td>
</tr>
<tr class="even">
<td>Simple <code>           for         </code> loop</td>
<td><pre><code>          
            for i in 1:10println(i)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Unnested <code>           for         </code> loop</td>
<td><pre><code>          
            for i in 1:10, j = 1:5println(i*j)end
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Enumeration</td>
<td><pre><code>          
            for (idx, val) in enumerate(arr)println(&quot;the $idx-th element is $val&quot;)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td><code>           while         </code> loop</td>
<td><pre><code>          
            while bool_expr# do stuffend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Exit loop</td>
<td><code>           break         </code></td>
</tr>
<tr class="odd">
<td>Exit iteration</td>
<td><code>           continue         </code></td>
</tr>
</tbody>
</table>
