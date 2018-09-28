For ` dplyr ` -like tools, see
[DataFramesMeta.jl.](https://github.com/JuliaStats/DataFramesMeta.jl)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Read CSV</td>
<td><pre><code>          
            using CSVCSV.read(filename)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Write CSV</td>
<td><pre><code>          
            using CSVCSV.write(filename)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Read Stata, SPSS, etc.</td>
<td><pre><code>          
            StatFiles
          
          Package
        </code></pre></td>
</tr>
<tr class="even">
<td><a href="#" class="tooltip">Describe <span> Similar to <code>               summary(df)             </code> in R. </span></a> data frame</td>
<td><code>           describe(df)         </code></td>
</tr>
<tr class="odd">
<td>Make vector of column <code>           col         </code></td>
<td><code>           v = df[:col]         </code></td>
</tr>
<tr class="even">
<td>Sort by <code>           col         </code></td>
<td><code>           sort!(df, [:col])         </code></td>
</tr>
<tr class="odd">
<td><a href="#" class="tooltip">Categorical <span> Similar to <code>               df$col = as.factor(df$col)             </code> in R. </span></a> <code>           col         </code></td>
<td><code>           categorical!(df, [:col])         </code></td>
</tr>
<tr class="even">
<td>List <code>           col         </code> levels</td>
<td><code>           levels(df[:col])         </code></td>
</tr>
<tr class="odd">
<td>All observations with <code>           col==val         </code></td>
<td><code>           df[df[:col] .== val, :]         </code></td>
</tr>
<tr class="even">
<td>Reshape from wide to long format</td>
<td><pre><code>          
            stack(df, [1:n; ])stack(df, [:col1, :col2, ...]melt(df, [:col1, :col2]) [
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Reshape from long to wide format</td>
<td><pre><code>          
            unstack(df, :id, :val)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Make Nullable</td>
<td><pre><code>          
            allowmissing!(df)
          
          or
          
            allowmissing!(df, :col)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Loop over Rows</td>
<td><pre><code>          
            for r in eachrow(df) # do stuff. # r is Struct with fields of col names.end
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Loop over Columns</td>
<td><pre><code>          
            for c in eachcol(df) # do stuff. # c is tuple with name, then vectorend
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Apply <code>           func         </code> to groups</td>
<td><code>           by(df, :group_col, func)         </code></td>
</tr>
<tr class="even">
<td>Query</td>
<td><pre><code>          
            using Queryquery = @from r in df begin     @where r.col1 &gt; 40     @select {new_name=r.col1, r.col2}     @collect DataFrame #Default: iterator     end
          
        </code></pre></td>
</tr>
</tbody>
</table>
