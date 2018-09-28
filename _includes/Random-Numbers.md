Many random number functions are require ` using Random ` .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Set seed</td>
<td><code>           seed!(seed)         </code></td>
</tr>
<tr class="even">
<td>Random numbers</td>
<td><pre><code>          
            rand()   # uniform [0,1)randn()  # normal (-Inf, Inf)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Random from Other Distribution</td>
<td><pre><code>          
            using Distributionsmy_dist = Bernoulli(0.2) # For examplerand(my_dist)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Random subsample elements from A with inclusion probability p</td>
<td><code>           randsubseq(A, p)         </code></td>
</tr>
<tr class="odd">
<td>Random permutation elements of A</td>
<td><code>           shuffle(A)         </code></td>
</tr>
</tbody>
</table>
