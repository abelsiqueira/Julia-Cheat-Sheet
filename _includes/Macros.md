Macros allow generated code (i.e. expressions) to be included in a
program.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Definition</td>
<td><pre><code>          
            macro macroname(expr)# do stuffend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Usage</td>
<td><code>           @macroname(ex1, ex2, ...)         </code> or <code>           @macroname                      ex1, ex2, ...         </code></td>
</tr>
<tr class="odd">
<td>Built-in macros</td>
<td><pre><code>          
            @test           # equal (exact)@test_approx_eq # equal (modulo numerical errors)@test x ≈ y     # isapprox(x, y)@assert         # assert (unit test)@which          # types used@time           # time and memory statistics@elapsed        # time elapsed@allocated      # memory allocated@profile        # profile@spawn          # run at some worker@spawnat        # run at specified worker@async          # asynchronous task@parallel       # parallel for loop@everywhere     # make available to workers
          
        </code></pre></td>
</tr>
</tbody>
</table>

Rules for creating *hygienic* macros:

  - Declare variables inside macro with ` local ` .
  - Do not call ` eval ` inside macro.
  - Escape interpolated expressions to avoid expansion: ` $(esc(expr)) `
    .
