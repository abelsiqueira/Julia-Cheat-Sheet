Julia is homoiconic: programs are represented as data structures of the
language itself. In fact, everything is an expression ` Expr ` .

Symbols are [interned strings <span> Only one copy of each distinct
(immutable) string value is stored. </span>](#) prefixed with a colon.
Symbols are more efficient and they are typically used as identifiers,
keys (in dictionaries), or columns in data frames. Symbols cannot be
concatenated.

Quoting ` :( ... ) ` or ` quote ... end ` creates an expression, just
like [` parse(str) ` <span> This form is probably most familiar to
people with knowledge of dynamic SQL. The ` parse ` function is similar
to Oracle"s and PostgreSQL"s ` EXECUTE IMMEDIATE ` statement or SQL
Server"s ` sp_executesql() ` procedure. </span>](#) , and ` Expr(:call,
...) ` .

<div class="indented">

``` 
    
      x = 1line = "1 + $x"      # some codeexpr = parse(line)   # make an Expr objecttypeof(expr) == Expr # truedump(expr)           # generate abstract syntax treeeval(expr) == 2      # evaluate Expr object: true
    
  
```

</div>
