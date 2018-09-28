<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Read stream</td>
<td><pre><code>          
            stream = stdinfor line in eachline(stream)# do stuffend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Read file</td>
<td><pre><code>          
            open(filename) do filefor line in eachline(file) # do stuffendend
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Read CSV file</td>
<td><pre><code>          
            using CSVCSV.read(filename)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Save Julia Object</td>
<td><pre><code>          
            using JLDsave(filename, &quot;object_key&quot;, object, ...)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Load Julia Object</td>
<td><pre><code>          
            using JLDd = load(filename) # Returns a dict of objects
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Save HDF5</td>
<td><pre><code>          
            using HDF5h5write(filename, &quot;key&quot;, object)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Load HDF5</td>
<td><pre><code>          
            using HDF5h5read(filename, &quot;key&quot;)
          
        </code></pre></td>
</tr>
</tbody>
</table>
