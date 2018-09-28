Modules are separate global variable workspaces that group together
similar functionality.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Definition</td>
<td><pre><code>          
            module PackageName# add module definitions# use export to make definitions accessibleend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Include <code>           filename.jl         </code></td>
<td><code>           include(&quot;filename.jl&quot;)         </code></td>
</tr>
<tr class="odd">
<td>Load</td>
<td><pre><code>          
            using ModuleName        # all exported namesusing ModuleName: x, y  # only x, yusing ModuleName.x,   ModuleName.y:     # only x, yimport ModuleName       # only ModuleNameimport ModuleName: x, y # only x, yimport ModuleName.x,    ModuleName.y     # only x, y
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Exports</td>
<td><pre><code>          
            # Get an array of names exported by Modulenames(ModuleName)# include non-exports, deprecateds# and compiler-generated namesnames(ModuleName, all::Bool)#also show names explicitely imported from other modulesnames(ModuleName, all::Bool, imported::Bool)
          
        </code></pre></td>
</tr>
</tbody>
</table>

There is only one difference between ` using ` and ` import ` : with `
using ` you need to say ` function Foo.bar(.. ` to extend module ` Foo `
's function ` bar ` with a new method, but with ` import Foo.bar ` , you
only need to say ` function bar(... ` and it automatically extends
module ` Foo ` 's function ` bar ` .
