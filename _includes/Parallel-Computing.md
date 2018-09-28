<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Launch REPL with <code>           N         </code> workers</td>
<td><code>           julia -p N         </code></td>
</tr>
<tr class="even">
<td>Number of available workers</td>
<td><code>           nprocs()         </code></td>
</tr>
<tr class="odd">
<td>Add <code>           N         </code> workers</td>
<td><code>           addprocs(N)         </code></td>
</tr>
<tr class="even">
<td>See all worker ids</td>
<td><pre><code>          
            for pid in workers()println(pid)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Get id of executing worker</td>
<td><code>           myid()         </code></td>
</tr>
<tr class="even">
<td>Remove worker</td>
<td><code>           rmprocs(pid)         </code></td>
</tr>
<tr class="odd">
<td>Run <code>           f         </code> with arguments <code>           args         </code> on <code>           pid         </code></td>
<td><pre><code>          
            r = remotecall(f, pid, args...)# or:r = @spawnat pid f(args)...fetch(r)
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Run <code>           f         </code> with arguments <code>           args         </code> on <code>           pid         </code> (more efficient)</td>
<td><pre><code>          
            remotecall_fetch(f, pid, args...)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Run <code>           f         </code> with arguments <code>           args         </code> on any worker</td>
<td><code>           r = @spawn f(args) ... fetch(r)         </code></td>
</tr>
<tr class="even">
<td>Run <code>           f         </code> with arguments <code>           args         </code> on all workers</td>
<td><code>           r = [@spawnat w f(args) for w in workers()] ...                     fetch(r)         </code></td>
</tr>
<tr class="odd">
<td>Make <code>           expr         </code> available to all workers</td>
<td><code>           @everywhere expr         </code></td>
</tr>
<tr class="even">
<td>Parallel <code>           for         </code> loop with <a href="#" class="tooltip">reducer <span> A reducer combines the results from different (independent) workers. </span></a> function <code>           red         </code></td>
<td><pre><code>          
            sum = @parallel (red) for i in 1:10^6# do parallel stuffend
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Apply <code>           f         </code> to all elements in collection <code>           coll         </code></td>
<td><code>           pmap(f, coll)         </code></td>
</tr>
</tbody>
</table>

Workers are also known as concurrent/parallel processes.

Modules with parallel processing capabilities are best split into a
functions file that contains all the functions and variables needed by
all workers, and a driver file that handles the processing of data. The
driver file obviously has to import the functions file.

A non-trivial (word count) example of a reducer function is provided by
[Adam
DeConinck](https://blog.ajdecon.org/parallel-word-count-with-julia-an-interesting)
.
