<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Integer types</td>
<td><code>           IntN         </code> and <code>           UIntN         </code> , with <code>           N         </code> ∈ { <code>           8         </code> , <code>           16         </code> , <code>           32         </code> , <code>           64         </code> , <code>           128         </code> }<br />
<code>           BigInt         </code></td>
</tr>
<tr class="even">
<td>Floating-point types</td>
<td><code>           FloatN         </code> with <code>           N         </code> ∈ { <code>           16         </code> , <code>           32         </code> , <code>           64         </code> }<br />
<code>           BigFloat         </code></td>
</tr>
<tr class="odd">
<td>Minimum and maximum values by type</td>
<td><pre><code>          
            typemin(Int8)typemax(Int64)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Complex types</td>
<td><code>           Complex{T}         </code></td>
</tr>
<tr class="odd">
<td>Imaginary unit</td>
<td><code>           im         </code></td>
</tr>
<tr class="even">
<td>Machine precision</td>
<td><code>           eps() # same as eps(Float64)         </code></td>
</tr>
<tr class="odd">
<td>Rounding</td>
<td><pre><code>          
            round()  # floating-pointround(Int, x) # integer
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Type conversions</td>
<td><pre><code>          
            convert(TypeName, val) # attempt/errortypename(val)          # calls convert
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Global constants</td>
<td><pre><code>          
            pi      # 3.1415...π       # 3.1415...im      # real(im * im) == -1
          
        </code></pre></td>
</tr>
<tr class="even">
<td>More constants</td>
<td><code>           using Base.MathConstants         </code></td>
</tr>
</tbody>
</table>

Julia does *not* automatically check for numerical overflow. Use package
` SaferIntegers for ints with overflow checking `
