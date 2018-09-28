Julia has no classes and thus no class-specific methods.

Types are like classes without methods.

Abstract types can be subtyped but not instantiated.

Concrete types cannot be subtyped.

By default, ` struct ` s are immutable.

Immutable types enhance performance and are thread safe, as they can be
shared among threads without the need for synchronization.

Objects that may be one of a set of types are called ` Union ` types.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Type annotation</td>
<td><code>           var::TypeName         </code></td>
</tr>
<tr class="even">
<td>Type declaration</td>
<td><pre><code>          
            struct Programmer name::String birth_year::UInt16 fave_language::AbstractStringend
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Mutable type declaration</td>
<td>replace <code>           struct         </code> with <code>           mutable struct         </code></td>
</tr>
<tr class="even">
<td>Type alias</td>
<td><code>           const Nerd = Programmer         </code></td>
</tr>
<tr class="odd">
<td>Type constructors</td>
<td><code>           methods(TypeName)         </code></td>
</tr>
<tr class="even">
<td>Type instantiation</td>
<td><pre><code>          
            me = Programmer(&quot;Ian&quot;, 1984, &quot;Julia&quot;)me = Nerd(&quot;Ian&quot;, 1984, &quot;Julia&quot;)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Subtype declaration</td>
<td><pre><code>          
            abstract type Programmer name::AbstractString birth_year::UInt16 fave_language::AbstractStringend
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Parametric type</td>
<td><pre><code>          
            struct Point{T &lt;: Real} x::T y::Tendp = Point{Float64}(1,2)
          
        </code></pre></td>
</tr>
<tr class="odd">
<td>Union types</td>
<td><pre><code>          
            Union{Int, String}
          
        </code></pre></td>
</tr>
<tr class="even">
<td>Traverse type hierarchy</td>
<td><code>           supertype(TypeName)         </code> and <code>           subtypes(TypeName)         </code></td>
</tr>
<tr class="odd">
<td>Default supertype</td>
<td><code>           Any         </code></td>
</tr>
<tr class="even">
<td>All fields</td>
<td><code>           fieldnames(TypeName)         </code></td>
</tr>
<tr class="odd">
<td>All field types</td>
<td><code>           TypeName.types         </code></td>
</tr>
</tbody>
</table>

When a type is defined with an *inner* constructor, the default *outer*
constructors are not available and have to be defined manually if need
be. An inner constructor is best used to check whether the parameters
conform to certain (invariance) conditions. Obviously, these invariants
can be violated by accessing and modifying the fields directly, unless
the type is defined as immutable. The ` new ` keyword may be used to
create an object of the same type.

Type parameters are invariant, which means that ` Point{Float64} <:
Point{Real} ` is false, even though ` Float64 <: Real ` . Tuple types,
on the other hand, are covariant: ` Tuple{Float64} <: Tuple{Real} ` .

The type-inferred form of Julia's internal representation can be found
with ` code_typed() ` . This is useful to identify where ` Any ` rather
than type-specific native code is generated.
