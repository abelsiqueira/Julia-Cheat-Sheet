<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Declaration</td>
<td><code>           arr = Float64[]         </code></td>
</tr>
<tr class="even">
<td>Pre-allocation</td>
<td><code>           sizehint!(arr, 10^4)         </code></td>
</tr>
<tr class="odd">
<td>Access and assignment</td>
<td><code>           arr = Any[1,2]                      arr[1] = &quot;Some text&quot;         </code></td>
</tr>
<tr class="even">
<td>Comparison</td>
<td><pre><code>          
            a = [1:10; ]b = a      # b points to aa[1] = -99a == b     # true
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Copy elements (not address)</td>
<td><pre><code>          
            b = copy(a)b = deepcopy(a)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Select subarray from <code>           m         </code> to <code>           n         </code></td>
<td><code>           arr[n:m]         </code></td>
</tr>
<tr class="odd">
<td><code>           n         </code> -element array with <code>           0.0         </code> s</td>
<td><code>           zeros(n)         </code></td>
</tr>
<tr class="even">
<td><code>           n         </code> -element array with <code>           1.0         </code> s</td>
<td><code>           ones(n)         </code></td>
</tr>
<tr class="odd">
<td><code>           n         </code> -element array with <code>           #undef         </code> s</td>
<td><code>           Vector{Type}(undef,n)         </code></td>
</tr>
<tr class="even">
<td><code>           n         </code> equally spaced numbers from <code>           start         </code> to <code>           stop         </code></td>
<td><code>           range(start,stop=stop,length=n)         </code></td>
</tr>
<tr class="odd">
<td>Array with <code>           n         </code> random <code>           Int8         </code> elements</td>
<td><code>           rand(Int8, n)         </code></td>
</tr>
<tr class="even">
<td>Fill array with <code>           val         </code></td>
<td><code>           fill!(arr, val)         </code></td>
</tr>
<tr class="odd">
<td>Pop last element</td>
<td><code>           pop!(arr)         </code></td>
</tr>
<tr class="even">
<td>Pop <em>first</em> element</td>
<td><code>           popfirst!(a)         </code></td>
</tr>
<tr class="odd">
<td>Push <code>           val         </code> as last element</td>
<td><code>           push!(arr, val)         </code></td>
</tr>
<tr class="even">
<td>Push <code>           val         </code> as <em>first</em> element</td>
<td><code>           pushfirst!(arr, val)         </code></td>
</tr>
<tr class="odd">
<td>Remove element at index <code>           idx         </code></td>
<td><code>           deleteat!(arr, idx)         </code></td>
</tr>
<tr class="even">
<td>Sort</td>
<td><code>           sort!(arr)         </code></td>
</tr>
<tr class="odd">
<td>Append <code>           a         </code> with <code>           b         </code></td>
<td><code>           append!(a,b)         </code></td>
</tr>
<tr class="even">
<td>Check whether <code>           val         </code> is element</td>
<td><code>           in(val, arr)         </code> or <code>           val in arr         </code></td>
</tr>
<tr class="odd">
<td>Scalar product</td>
<td><code>           dot(a, b) == sum(a .* b)         </code></td>
</tr>
<tr class="even">
<td>Change dimensions (if possible)</td>
<td><pre><code>          
            reshape(1:6, 3, 2)&#39; ==[1 2 3; 4 5 6]
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>To string (with delimiter <code>           del         </code> between elements)</td>
<td><code>           join(arr, del)         </code></td>
</tr>
</tbody>
</table>
