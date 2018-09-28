<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Throw <code>           SomeExcep         </code></td>
<td><code>           throw(SomeExcep())         </code></td>
</tr>
<tr class="even">
<td>Rethrow current exception</td>
<td><code>           rethrow()         </code></td>
</tr>
<tr class="odd">
<td>Define <code>           NewExcep         </code></td>
<td><pre><code>          
            struct NewExcep &lt;: Exceptionv::StringendBase.showerror(io::IO, e::NewExcep) =print(io, &quot;A problem with $(e.v)!&quot;)throw(NewExcep(&quot;x&quot;))
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Throw error with <code>           msg         </code> text</td>
<td><code>           error(msg)         </code></td>
</tr>
<tr class="odd">
<td>Handler</td>
<td><pre><code>          
            try# do something potentially iffycatch exif isa(ex, SomeExcep) # handle SomeExcepelseif isa(ex, AnotherExcep) # handle AnotherExcepelse # handle all othersfinally # do this in any caseend
          
        </code></pre></td>
</tr>
</tbody>
</table>
