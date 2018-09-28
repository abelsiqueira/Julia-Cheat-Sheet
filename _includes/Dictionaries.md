<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Dictionary</td>
<td><pre><code>          
            d = Dict(key1 =&gt; val1,      key2 =&gt; val2, ...)d = Dict(:key1 =&gt; val1,      :key2 =&gt; val2, ...)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>All keys (iterator)</td>
<td><code>           keys(d)         </code></td>
</tr>
<tr class="odd">
<td>All values (iterator)</td>
<td><code>           values(d)         </code></td>
</tr>
<tr class="even">
<td>Loop through key-value pairs</td>
<td><pre><code>          
            for (k,v) in dprintln(&quot;key: $k, value: $v&quot;)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Check for key <code>           :k         </code></td>
<td><code>           haskey(d, :k)         </code></td>
</tr>
<tr class="even">
<td>Copy keys (or values) to array</td>
<td><pre><code>          
            arr = collect(keys(d))arr = [k for (k,v) in d]
          
        </code></pre></td>
</tr>
</tbody>
</table>

Dictionaries are mutable; when symbols are used as keys, the keys are
immutable.
