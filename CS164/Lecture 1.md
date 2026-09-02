
## What is a Compiler?

Compiler : source program -> target program

Examples
GCC : C/C++ -> assembly code
Javac : Java -> Java codebytes

![[Pasted image 20260901210147.png]]


Open ocaml intepreter
```
dune utop
```

mov rax, 12
operation destination, source

"Default: " ^ x
*carot is for concatenation*


## Common Ocaml Mistake
With a nested match/switch statement
![[Pasted image 20260902105036.png]]
Ocaml is not white space sensitive

Solution: use paranthesis

The issue is likely that OCaml is treating the nested match’s `|` branches as part of the outer match. Wrap the inner `match` in parentheses:

```
match outer_value with
| OuterCase x ->
    (match inner_value with
     | InnerCase1 -> result1
     | InnerCase2 -> result2)
| AnotherOuterCase ->
    result3
```

You can also use `begin ... end`:

```
match outer_value with
| OuterCase x ->
    begin
      match inner_value with
      | InnerCase1 -> result1
      | InnerCase2 -> result2
    end
| AnotherOuterCase ->
    result3
```

Every `match` needs at least one branch beginning with `|`. Paste your exact code and error message, and I can restructure it directly.