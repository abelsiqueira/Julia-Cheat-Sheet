Tasks provide a lightweight threading mechanism and they can be
suspended and resumed at will. Tasks follow the producer-consumer model,
which means that between consumption calls the task is suspended.

Tasks are *not* executed in different threads, so they cannot run on
different processors.

Tasks have low overhead because switching between them does not consume
stack space unlike normal function calls.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Define</td>
<td><code>           t = Task( () -&gt; somefunc(...) )         </code> or <code>           t                     = @task somefunc(...)         </code></td>
</tr>
<tr class="even">
<td>Produce</td>
<td><pre><code>          
            function somefunc(...)# do stuffproduce(...)end
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Consume</td>
<td><code>           consume(t)         </code></td>
</tr>
</tbody>
</table>
