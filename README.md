# Python Interview Questions

Questions, answers, and code examples for Python interviews — from junior to senior level.

795 questions · 51 subtopics

Full answers and code examples: [interview-prep.coderboi.com/python](https://interview-prep.coderboi.com/python)  
Structured study roadmap: [interview-prep.coderboi.com/roadmap/python](https://interview-prep.coderboi.com/roadmap/python)

---

I put this together while preparing for backend engineering roles. Most question banks online either stop at the basics or dump a list with no real answers. This one goes deeper.

Every question has a full written answer with working code on the linked page. The questions here are the exact ones I kept getting asked, or the ones I kept getting wrong.

---

## Index

**[Fundamentals](#fundamentals)** — 95 questions  
[Mutability & Data Types](#mutability--data-types) · [Variables, Scope & the LEGB Rule](#variables-scope--the-legb-rule) · [Numbers & Operators](#numbers--operators) · [Strings & String Formatting](#strings--string-formatting) · [Truthiness & Type Conversion](#truthiness--type-conversion)

**[Functions](#functions)** — 61 questions  
[Decorators](#decorators) · [Function Arguments](#function-arguments) · [Closures & Scope](#closures--scope) · [Lambdas & Higher-Order Functions](#lambdas--higher-order-functions)

**[OOP](#oop)** — 90 questions  
[Inheritance & the MRO](#inheritance--the-mro) · [Classes, Instances & \_\_init\_\_](#classes-instances--__init__) · [Dunder / Magic Methods](#dunder--magic-methods) · [Methods & Properties](#methods--properties) · [Dataclasses & \_\_slots\_\_](#dataclasses--__slots__) · [Abstract Base Classes & Protocols](#abstract-base-classes--protocols)

**[Data Structures](#data-structures)** — 78 questions  
[Lists & Slicing](#lists--slicing) · [Tuples & Named Tuples](#tuples--named-tuples) · [Dictionaries](#dictionaries) · [Sets & Frozensets](#sets--frozensets) · [The collections Module](#the-collections-module)

**[Iteration](#iteration)** — 60 questions  
[Generators & yield](#generators--yield) · [List, Dict & Set Comprehensions](#list-dict--set-comprehensions) · [Iterators & the Iterator Protocol](#iterators--the-iterator-protocol) · [enumerate, zip & Unpacking](#enumerate--zip--unpacking)

**[Functional](#functional)** — 48 questions  
[functools](#functools) · [map, filter & reduce](#map-filter--reduce) · [itertools](#itertools)

**[Exceptions](#exceptions)** — 46 questions  
[Context Managers & with](#context-managers--with) · [try / except / else / finally](#try--except--else--finally) · [Custom Exceptions & the Hierarchy](#custom-exceptions--the-hierarchy)

**[Concurrency](#concurrency)** — 62 questions  
[Threading & the GIL](#threading--the-gil) · [Multiprocessing](#multiprocessing) · [asyncio & async/await](#asyncio--asyncawait) · [concurrent.futures](#concurrentfutures)

**[Modules](#modules)** — 45 questions  
[The Import System](#the-import-system) · [Packages & \_\_main\_\_](#packages--__main__) · [Virtual Environments & pip](#virtual-environments--pip)

**[Typing](#typing)** — 30 questions  
[Type Hints & Annotations](#type-hints--annotations) · [Generics & Protocols](#generics--protocols)

**[Standard Library](#standard-library)** — 60 questions  
[Regular Expressions](#regular-expressions) · [Files, pathlib & os](#files-pathlib--os) · [datetime](#datetime) · [JSON, CSV & pickle](#json-csv--pickle)

**[Internals](#internals)** — 45 questions  
[Garbage Collection & Reference Counting](#garbage-collection--reference-counting) · [Identity, is vs ==, & Interning](#identity-is-vs---interning) · [The CPython Execution Model](#the-cpython-execution-model)

**[Idioms](#idioms)** — 45 questions  
[EAFP vs LBYL](#eafp-vs-lbyl) · [PEP 8 & Style](#pep-8--style) · [Common Gotchas & Anti-patterns](#common-gotchas--anti-patterns)

**[Testing](#testing)** — 30 questions  
[pytest Essentials](#pytest-essentials) · [Mocking & Patching](#mocking--patching)

---

## Fundamentals

The questions that sort out candidates who actually understand Python from those who just use it.

### Mutability & Data Types

- 🟢 [Which Python types are mutable and which are immutable?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-mutable-immutable)
- 🔴 [What is the mutable default argument trap?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-default-arg)
- 🟡 [What is the difference between `is` and `==`?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-is-vs-eq)
- 🟡 [What is the difference between a shallow and a deep copy?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-shallow-deep-copy)
- 🟡 [Can a tuple contain mutable objects?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-tuple-mutable)
- 🔴 [Why can't you use a list as a dictionary key?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-hashable)
- 🟡 [What does the id() function tell you?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-id-function)
- 🔴 [Why does `is` sometimes work for equal integers?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-small-int-cache)
- 🔴 [What is string interning in Python?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-string-interning)
- 🔴 [What happens when you use += on a list inside a tuple?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-augmented-tuple)
- 🟡 [Does slicing a list create a copy?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-list-slicing-copy)
- 🔴 [Is Python pass-by-value or pass-by-reference?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-pass-by-object)
- 🔴 [How does deepcopy handle circular references?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-deepcopy-cycles)
- 🟡 [When is using `is` instead of `==` a bug?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-is-pitfall)
- 🔴 [How do you make a custom class hashable?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-custom-hashable)
- 🟡 [What is a frozen dataclass?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-frozen-dataclass)
- 🟢 [Why are strings immutable in Python?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-string-immutability)
- 🟡 [What is the difference between a tuple and a list?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-tuple-vs-list)
- 🔴 [What happens if you modify a list while iterating over it?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-mutate-during-iteration)
- 🟡 [What does the del statement do?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-del-statement)
- 🟡 [What is the difference between rebinding and mutating?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-rebind-vs-mutate)
- 🔴 [Why is a mutable class attribute shared across instances?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-class-mutable-attr)
- 🔴 [What is the trap with [[]] * 3?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-list-mult-trap)
- 🟡 [What is a namedtuple and when do you use it?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-namedtuple)
- 🔴 [What do the global and nonlocal keywords do?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-global-nonlocal)
- 🟢 [What are the ways to copy a list or dict?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-copy-methods)
- 🟢 [Why check for None with `is` rather than ==?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-none-identity)
- 🟡 [Why must set elements be hashable?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-set-hashable-elements)
- 🟡 [Do comprehensions leak their loop variable?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-comprehension-scope)
- 🟢 [How does tuple unpacking enable swapping variables?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-tuple-unpacking-swap)
- 🟡 [What is the trap with shallow-copying nested structures?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-shallow-nested-trap)
- 🟡 [What is a frozenset?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-frozenset)
- 🔴 [What is the relationship between __eq__ and __hash__?](https://interview-prep.coderboi.com/python/fundamentals/mutability#q-eq-hash-contract)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/fundamentals/mutability)

### Variables, Scope & the LEGB Rule

- 🟡 [What is the LEGB rule?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-legb-rule)
- 🟡 [What is the difference between `global` and `nonlocal`?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-global-vs-nonlocal)
- 🔴 [Why does assigning to a name make it local and cause UnboundLocalError?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-unbound-local-error)
- 🔴 [Why do closures in a loop all capture the same value?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-late-binding-closures)
- 🟡 [How does name shadowing work between module and function scope?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-module-vs-function-shadowing)
- 🟡 [Do comprehensions have their own scope?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-comprehension-scope)
- 🔴 [How can you inspect what a closure has captured?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-closure-cell-vars)
- 🟡 [In which scope are default argument values evaluated?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-default-arg-evaluation-scope)
- 🟡 [What do the `globals()` and `locals()` functions return?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-globals-locals-functions)
- 🟡 [Can a nested function read an enclosing variable without `nonlocal`?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-nested-function-scope-lookup)
- 🔴 [Why can't methods see class-body variables directly?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-class-body-scope)
- 🟡 [What does `del` do to a name's scope?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-del-and-scope)
- 🟡 [What happens if you assign to a built-in name at module level?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-builtins-override)
- 🔴 [What is a "free variable" and how does it differ from a global?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-free-variable-vs-global)
- 🟡 [Why does patching a global affect already-defined functions but rebinding a local doesn't?](https://interview-prep.coderboi.com/python/fundamentals/scope-legb#q-monkeypatch-module-scope)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/fundamentals/scope-legb)

### Numbers & Operators

- 🟢 [What are Python's built-in numeric types?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-numeric-types)
- 🟡 [How do `/`, `//`, and `%` behave, especially with negatives?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-division-floor-modulo)
- 🟢 [Why don't Python integers overflow?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-int-arbitrary-precision)
- 🟡 [Why is 0.1 + 0.2 not exactly 0.3?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-float-precision-decimal)
- 🟡 [What are Python's bitwise operators?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-bitwise-operators)
- 🟢 [What do `divmod` and `**` do?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-divmod-and-power)
- 🟢 [How does `bool` relate to `int` in arithmetic?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-bool-is-int)
- 🟢 [How do `int()`, `float()`, and `round()` differ in converting numbers?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-int-float-conversion)
- 🟡 [How do chained comparisons like `a < b < c` work?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-chained-comparisons)
- 🟡 [Is `x += 1` the same as `x = x + 1`?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-augmented-assignment-numbers)
- 🟢 [When should you use the `math` module instead of operators?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-math-vs-operators)
- 🔴 [What is special about `float('nan')`?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-nan-behavior)
- 🟡 [Why does `a is b` sometimes work for equal integers?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-integer-caching)
- 🟢 [How do you work with complex numbers?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-complex-numbers-usage)
- 🟡 [How do you format numbers for display?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-number-formatting)
- 🟢 [What do underscores in numeric literals do?](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators#q-underscore-numeric-literals)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/fundamentals/numbers-operators)

### Strings & String Formatting

- 🟡 [What is the difference between f-strings, .format(), and % formatting?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-fstring-vs-format-vs-percent)
- 🟡 [What is the difference between str and bytes?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-str-vs-bytes)
- 🟢 [What are the common string methods like split, strip, and join?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-common-string-methods)
- 🟡 [Why use join instead of += to build a string in a loop?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-join-vs-concat-loop)
- 🟢 [What is a raw string and when do you use it?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-raw-strings)
- 🟡 [How does the format spec mini-language work (padding, :.2f)?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-format-spec-mini-language)
- 🟢 [What does it mean that strings are immutable?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-string-immutability)
- 🟢 [How do you check for substrings and find their positions?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-string-membership-and-search)
- 🟢 [What string methods test or change case and content type?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-string-case-and-test-methods)
- 🔴 [Why might two visually identical strings compare unequal?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-unicode-normalization)
- 🟢 [How does string slicing work, including negative steps?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-string-slicing)
- 🟡 [What do `!r`, `!s`, and `=` do inside f-strings?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-fstring-conversion-and-debug)
- 🟢 [How do triple-quoted strings and implicit concatenation work?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-multiline-and-implicit-concat)
- 🟡 [How do you efficiently replace or delete many characters at once?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-translate-and-maketrans)
- 🟡 [When would you use `partition` instead of `split`?](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting#q-partition-vs-split)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/fundamentals/strings-formatting)

### Truthiness & Type Conversion

- 🟢 [Which values are falsy in Python?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-falsy-values)
- 🟡 [How does Python decide whether a custom object is truthy?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-bool-len-protocol)
- 🟢 [How do explicit type conversions like int(), str(), and list() work?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-explicit-conversion)
- 🟢 [Are empty containers and None falsy?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-empty-container-truthiness)
- 🟡 [What do `and` and `or` actually return?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-and-or-short-circuit)
- 🟢 [Why use `is None` instead of `== None`?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-is-none-vs-eq-none)
- 🟡 [Why can `if x:` be a bug when you mean `if x is not None:`?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-truthy-vs-explicit-empty-check)
- 🟢 [How does `bool()` convert numbers and strings?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-bool-int-conversion)
- 🟡 [How do `any()` and `all()` use truthiness?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-any-all-functions)
- 🟡 [When does Python convert numeric types implicitly?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-implicit-numeric-conversion)
- 🔴 [Does `if a == b == c` compare truthiness or values?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-comparison-chaining-truthiness)
- 🟢 [How do you convert between number bases?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-number-base-conversion)
- 🟡 [What surprises happen when converting between containers?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-container-conversion-pitfalls)
- 🟡 [What is the difference between `str()` and `repr()`?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-str-vs-repr-conversion)
- 🟢 [How do you convert between characters and their code points?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-ascii-ord-chr)
- 🔴 [Is `float('nan')` truthy or falsy?](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion#q-nan-truthiness)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/fundamentals/truthiness-conversion)

---

## Functions

Decorators and closures trip up almost everyone. Make sure you can explain the full execution model.

### Decorators

- 🟡 [What is a decorator and how does it work?](https://interview-prep.coderboi.com/python/functions/decorators#q-what-is-decorator)
- 🔴 [Why should you use functools.wraps in a decorator?](https://interview-prep.coderboi.com/python/functions/decorators#q-functools-wraps)
- 🔴 [How do you write a decorator that takes arguments?](https://interview-prep.coderboi.com/python/functions/decorators#q-decorator-with-arguments)
- 🔴 [How do you implement a decorator as a class?](https://interview-prep.coderboi.com/python/functions/decorators#q-class-based-decorator)
- 🟡 [When you stack multiple decorators, in what order do they apply?](https://interview-prep.coderboi.com/python/functions/decorators#q-stacking-decorators)
- 🟢 [What does the @ decorator syntax desugar to?](https://interview-prep.coderboi.com/python/functions/decorators#q-decorator-syntax-sugar)
- 🟡 [What breaks if you forget functools.wraps in a decorator?](https://interview-prep.coderboi.com/python/functions/decorators#q-preserve-metadata)
- 🔴 [How do you write a decorator that works with or without arguments?](https://interview-prep.coderboi.com/python/functions/decorators#q-decorator-with-without-args)
- 🟡 [Can you decorate a class, and what does a class decorator do?](https://interview-prep.coderboi.com/python/functions/decorators#q-class-decorator)
- 🟡 [In what order do stacked decorators apply?](https://interview-prep.coderboi.com/python/functions/decorators#q-stacking-order)
- 🟡 [How is property a decorator?](https://interview-prep.coderboi.com/python/functions/decorators#q-property-as-decorator)
- 🟡 [When does a decorator's code run?](https://interview-prep.coderboi.com/python/functions/decorators#q-decorator-side-effects)
- 🟡 [How do staticmethod and classmethod work as decorators?](https://interview-prep.coderboi.com/python/functions/decorators#q-staticmethod-classmethod-decorators)
- 🟡 [How can a decorator maintain state across calls?](https://interview-prep.coderboi.com/python/functions/decorators#q-decorator-state)
- 🔴 [What is the three-level structure of a decorator with arguments?](https://interview-prep.coderboi.com/python/functions/decorators#q-parametrized-decorator-structure)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functions/decorators)

### Function Arguments

- 🟡 [What do *args and **kwargs do?](https://interview-prep.coderboi.com/python/functions/arguments#q-args-kwargs)
- 🟢 [What is the difference between positional and keyword arguments?](https://interview-prep.coderboi.com/python/functions/arguments#q-positional-vs-keyword)
- 🟢 [How do default argument values work?](https://interview-prep.coderboi.com/python/functions/arguments#q-default-args)
- 🟡 [What are keyword-only arguments?](https://interview-prep.coderboi.com/python/functions/arguments#q-keyword-only)
- 🔴 [What are positional-only parameters?](https://interview-prep.coderboi.com/python/functions/arguments#q-positional-only)
- 🟡 [What is the correct order of parameters in a signature?](https://interview-prep.coderboi.com/python/functions/arguments#q-param-ordering)
- 🟡 [Why is a mutable default argument dangerous?](https://interview-prep.coderboi.com/python/functions/arguments#q-mutable-default-arg)
- 🟡 [How do * and ** work at the call site?](https://interview-prep.coderboi.com/python/functions/arguments#q-unpacking-call)
- 🔴 [Does Python pass arguments by value or by reference?](https://interview-prep.coderboi.com/python/functions/arguments#q-pass-by-object)
- 🟡 [Does **kwargs preserve order?](https://interview-prep.coderboi.com/python/functions/arguments#q-kwargs-order)
- 🟡 [What does a bare `*` in a signature do?](https://interview-prep.coderboi.com/python/functions/arguments#q-bare-star)
- 🔴 [What does the `/` in a signature mean?](https://interview-prep.coderboi.com/python/functions/arguments#q-slash-positional-only)
- 🟢 [What is the difference between a parameter and an argument?](https://interview-prep.coderboi.com/python/functions/arguments#q-arg-vs-param)
- 🟡 [How do you forward arbitrary arguments to another function?](https://interview-prep.coderboi.com/python/functions/arguments#q-forwarding-args)
- 🟢 [When should you call with keyword arguments even if positional is allowed?](https://interview-prep.coderboi.com/python/functions/arguments#q-keyword-arg-clarity)
- 🟡 [When are default argument values evaluated?](https://interview-prep.coderboi.com/python/functions/arguments#q-default-eval-time)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functions/arguments)

### Closures & Scope

- 🔴 [What is a closure and what are free variables?](https://interview-prep.coderboi.com/python/functions/closures#q-what-is-a-closure)
- 🟡 [What does the nonlocal keyword do?](https://interview-prep.coderboi.com/python/functions/closures#q-nonlocal)
- 🔴 [Why do closures in a loop all capture the same value?](https://interview-prep.coderboi.com/python/functions/closures#q-late-binding)
- 🔴 [How can you inspect a closure's captured variables?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-cell)
- 🟡 [When should you use a closure instead of a class?](https://interview-prep.coderboi.com/python/functions/closures#q-closures-vs-classes)
- 🟡 [How do you fix closures in a loop capturing the same value?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-loop-fix)
- 🟡 [Why prefer a closure over a global variable for shared state?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-vs-global)
- 🔴 [What does "closures capture variables, not values" mean?](https://interview-prep.coderboi.com/python/functions/closures#q-late-binding)
- 🔴 [How does Python implement closures under the hood?](https://interview-prep.coderboi.com/python/functions/closures#q-cell-objects)
- 🟡 [What is the difference between nonlocal and global?](https://interview-prep.coderboi.com/python/functions/closures#q-nonlocal-vs-global)
- 🟡 [How do you build a simple memoizer with a closure?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-memoization)
- 🟡 [What is a function factory?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-factory)
- 🔴 [Why does assigning to an enclosed variable without nonlocal raise UnboundLocalError?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-gotcha-rebind)
- 🟡 [Do closures keep captured objects alive?](https://interview-prep.coderboi.com/python/functions/closures#q-closures-keep-alive)
- 🟡 [What's the difference between capturing via closure and via default argument?](https://interview-prep.coderboi.com/python/functions/closures#q-closure-vs-default-arg)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functions/closures)

### Lambdas & Higher-Order Functions

- 🟢 [What is a lambda and what are its limitations?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-syntax)
- 🟡 [When should you use a lambda versus a def?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-vs-def)
- 🟡 [What is a higher-order function?](https://interview-prep.coderboi.com/python/functions/lambdas#q-higher-order-functions)
- 🟡 [How does the key argument work in sorted, max, and min?](https://interview-prep.coderboi.com/python/functions/lambdas#q-key-argument)
- 🟡 [What does it mean that functions are first-class objects?](https://interview-prep.coderboi.com/python/functions/lambdas#q-first-class-functions)
- 🟢 [Why can't a lambda contain statements?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-single-expression)
- 🟡 [Can a lambda use conditionals or the walrus operator?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-walrus)
- 🟡 [Why does PEP 8 discourage assigning a lambda to a name?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-naming-pep8)
- 🟢 [What are good uses for a lambda?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-as-callback)
- 🟡 [Do lambdas capture variables the same way as nested functions?](https://interview-prep.coderboi.com/python/functions/lambdas#q-lambda-closure-capture)
- 🟡 [When should you use the operator module instead of a lambda?](https://interview-prep.coderboi.com/python/functions/lambdas#q-operator-module-vs-lambda)
- 🟡 [What does it mean for a higher-order function to return a function?](https://interview-prep.coderboi.com/python/functions/lambdas#q-hof-returning)
- 🟢 [Should you pair lambdas with map and filter?](https://interview-prep.coderboi.com/python/functions/lambdas#q-map-filter-with-lambda)
- 🟡 [What practical patterns do first-class functions enable?](https://interview-prep.coderboi.com/python/functions/lambdas#q-first-class-uses)
- 🟡 [How can an object behave like a function?](https://interview-prep.coderboi.com/python/functions/lambdas#q-callable-objects)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functions/lambdas)

---

## OOP

Python's OOP has quirks that don't exist in Java or C#. Dunder methods and descriptors come up constantly.

### Inheritance & the MRO

- 🟢 [What is the difference between single and multiple inheritance?](https://interview-prep.coderboi.com/python/oop/inheritance#q-single-vs-multiple)
- 🔴 [What is the MRO and how is it computed?](https://interview-prep.coderboi.com/python/oop/inheritance#q-what-is-mro)
- 🔴 [How does super() actually work?](https://interview-prep.coderboi.com/python/oop/inheritance#q-how-super-works)
- 🔴 [What is the diamond problem and how does Python solve it?](https://interview-prep.coderboi.com/python/oop/inheritance#q-diamond-problem)
- 🟡 [What are mixins and abstract base classes?](https://interview-prep.coderboi.com/python/oop/inheritance#q-mixins-and-abc)
- 🔴 [How should `__init__` cooperate with `super()` across a multiple-inheritance chain?](https://interview-prep.coderboi.com/python/oop/inheritance#q-super-init-args)
- 🟡 [Why prefer `isinstance` over `type(x) == SomeClass`?](https://interview-prep.coderboi.com/python/oop/inheritance#q-isinstance-vs-type)
- 🟢 [How do you override a method while still using the parent's version?](https://interview-prep.coderboi.com/python/oop/inheritance#q-method-override-and-extend)
- 🟡 [When should you favor composition over inheritance?](https://interview-prep.coderboi.com/python/oop/inheritance#q-composition-vs-inheritance)
- 🔴 [What does `__init_subclass__` let a base class do?](https://interview-prep.coderboi.com/python/oop/inheritance#q-subclass-hooks)
- 🟡 [How does attribute lookup use the MRO for class attributes?](https://interview-prep.coderboi.com/python/oop/inheritance#q-name-resolution-attributes)
- 🔴 [What is the difference between `super()` and `super(Class, self)`?](https://interview-prep.coderboi.com/python/oop/inheritance#q-super-with-args)
- 🟡 [Does Python support method overloading like Java?](https://interview-prep.coderboi.com/python/oop/inheritance#q-overriding-vs-overloading)
- 🟡 [Can you partially implement an abstract base class in an intermediate subclass?](https://interview-prep.coderboi.com/python/oop/inheritance#q-abstract-cannot-instantiate)
- 🔴 [How does `super()` behave inside a classmethod?](https://interview-prep.coderboi.com/python/oop/inheritance#q-super-in-classmethod)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/inheritance)

### Classes, Instances & __init__

- 🟢 [What is the difference between a class and an instance?](https://interview-prep.coderboi.com/python/oop/classes#q-class-vs-instance)
- 🟡 [What is the difference between __init__ and __new__?](https://interview-prep.coderboi.com/python/oop/classes#q-init-vs-new)
- 🟢 [What is `self` in Python?](https://interview-prep.coderboi.com/python/oop/classes#q-what-is-self)
- 🟡 [What is the difference between instance and class attributes?](https://interview-prep.coderboi.com/python/oop/classes#q-instance-vs-class-attributes)
- 🟡 [What is the difference between __repr__ and __str__?](https://interview-prep.coderboi.com/python/oop/classes#q-repr-vs-str)
- 🟡 [What happens, step by step, when you call ClassName()?](https://interview-prep.coderboi.com/python/oop/classes#q-object-creation-flow)
- 🟡 [Where does an instance store its attributes?](https://interview-prep.coderboi.com/python/oop/classes#q-instance-dict)
- 🟡 [What is the difference between `@classmethod` and `@staticmethod`?](https://interview-prep.coderboi.com/python/oop/classes#q-class-method-vs-static-method)
- 🟡 [How do `getattr`, `setattr`, and `hasattr` work?](https://interview-prep.coderboi.com/python/oop/classes#q-dynamic-attributes)
- 🟢 [Can `__init__` return a value?](https://interview-prep.coderboi.com/python/oop/classes#q-init-no-return)
- 🔴 [What happens to hashing when you define `__eq__`?](https://interview-prep.coderboi.com/python/oop/classes#q-equality-and-hash)
- 🟡 [What does a double-underscore prefix like `__name` do?](https://interview-prep.coderboi.com/python/oop/classes#q-name-mangling)
- 🟡 [What is a bound method versus accessing a function on the class?](https://interview-prep.coderboi.com/python/oop/classes#q-bound-vs-unbound-methods)
- 🔴 [In what sense is a class itself an object?](https://interview-prep.coderboi.com/python/oop/classes#q-class-as-object)
- 🔴 [What does `__del__` do and why is it unreliable?](https://interview-prep.coderboi.com/python/oop/classes#q-del-and-finalizer)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/classes)

### Dunder / Magic Methods

- 🟡 [What are dunder (magic) methods?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-what-are-dunder-methods)
- 🟡 [How do __repr__ and __str__ control how an object prints?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-repr-str-dunder)
- 🔴 [How do __eq__ and __hash__ work together?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-eq-and-hash)
- 🔴 [How do you overload operators like + and *?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-operator-overloading)
- 🔴 [How do __len__ and __getitem__ make an object behave like a sequence?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-sequence-protocol)
- 🟡 [What does __call__ do?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-call-dunder)
- 🟡 [What does functools.total_ordering do?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-total-ordering)
- 🔴 [What is the difference between `__getattr__` and `__getattribute__`?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-getattr-vs-getattribute)
- 🟡 [How does `__setattr__` work and how do you avoid infinite recursion?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-setattr-dunder)
- 🟡 [Which dunders make an object usable in a `with` statement?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-context-manager-dunders)
- 🟡 [What is the difference between `__iter__` and `__next__`?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-iter-next-dunders)
- 🟢 [How do `__bool__` and `__len__` affect truthiness in `if obj:`?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-bool-and-len-dunder)
- 🔴 [When are reflected operators like `__radd__` called?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-reflected-operators)
- 🟡 [How does `__index__` differ from `__int__`?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-slots-dunder)
- 🟢 [How does `__contains__` customize the `in` operator?](https://interview-prep.coderboi.com/python/oop/dunder-methods#q-contains-dunder)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/dunder-methods)

### Methods & Properties

- 🟡 [What is the difference between an instance method, @classmethod, and @staticmethod?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-instance-class-static-methods)
- 🟡 [How do you use a classmethod as an alternative constructor?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-classmethod-constructor)
- 🟡 [How does @property work with a getter and setter?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-property-getter-setter)
- 🟡 [Why do properties beat Java-style getter/setter methods?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-why-properties-over-getters)
- 🟢 [How do you create a computed or read-only property?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-computed-readonly-properties)
- 🟡 [How does `functools.cached_property` differ from `@property`?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-cached-property)
- 🟡 [What does the `@x.deleter` of a property do?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-property-deleter)
- 🔴 [How is `@property` related to descriptors?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-property-as-descriptor)
- 🟡 [Why does setting `self.x = value` in `__init__` trigger the property setter?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-setter-validation-init)
- 🟡 [Can a `@staticmethod` or `@classmethod` be called on an instance?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-method-types-access)
- 🟡 [What happens when you store a bound method as a callback?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-bound-method-as-callback)
- 🔴 [Why prefer a classmethod over a staticmethod for a factory?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-classmethod-vs-staticmethod-subclass)
- 🟢 [When should something be a property versus a regular method?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-property-vs-method-call)
- 🟡 [How do you override a property in a subclass?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-abstract-property-override)
- 🔴 [What is the difference between `obj.method()` and `Class.method(obj)`?](https://interview-prep.coderboi.com/python/oop/methods-properties#q-instance-method-on-class)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/methods-properties)

### Dataclasses & __slots__

- 🟢 [What does the @dataclass decorator generate for you?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-what-dataclass-generates)
- 🟡 [What does frozen=True do on a dataclass?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-frozen-dataclass)
- 🔴 [Why must mutable dataclass defaults use field(default_factory=...)?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-default-factory)
- 🔴 [What is __slots__ and what does it buy you?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-slots)
- 🟡 [When would you choose a dataclass over a namedtuple or NamedTuple?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-dataclass-vs-namedtuple)
- 🟡 [What is __post_init__ used for?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-post-init)
- 🟡 [What can the `field()` function configure besides defaults?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-field-options)
- 🟢 [How do you convert a dataclass to a dict or tuple?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-asdict-astuple)
- 🔴 [What is the field-ordering rule when inheriting dataclasses?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-dataclass-inheritance)
- 🟡 [How does `kw_only=True` help with dataclass inheritance?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-kw-only-fields)
- 🔴 [What's a common pitfall combining `__slots__` with class-level defaults?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-slots-and-defaults-conflict)
- 🔴 [Why might `__slots__` not save memory in a subclass?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-slots-inheritance)
- 🟡 [What does `order=True` add to a dataclass?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-order-true)
- 🔴 [How do you sort a dataclass by a computed key with `order=True`?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-sort-index-pattern)
- 🟡 [How do dataclass, slotted dataclass, and NamedTuple compare on memory?](https://interview-prep.coderboi.com/python/oop/dataclasses-slots#q-namedtuple-vs-dict-memory)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/dataclasses-slots)

### Abstract Base Classes & Protocols

- 🟡 [What is an abstract base class and what does @abstractmethod do?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-what-is-abc)
- 🟡 [Why use ABCs instead of just regular classes?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-why-use-abcs)
- 🔴 [What is collections.abc and how is it useful?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-collections-abc)
- 🟡 [What is the difference between duck typing and ABCs?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-duck-typing-vs-abcs)
- 🔴 [What is typing.Protocol and how does it relate to duck typing?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-typing-protocol)
- 🔴 [How do you declare an abstract property or abstract classmethod?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-abstract-property)
- 🔴 [What does ABC `.register()` do?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-register-virtual-subclass)
- 🔴 [How does `__subclasshook__` enable structural isinstance checks?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-subclasshook)
- 🟡 [When should you choose a Protocol over an ABC?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-protocol-vs-abc-when)
- 🟡 [What is the difference between `NotImplemented` and `NotImplementedError`?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-notimplemented-vs-error)
- 🔴 [Why does `abc.ABC` exist when there's already `ABCMeta`?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-abc-metaclass)
- 🟡 [Can an abstract method have an implementation, and why would it?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-abstractmethod-with-body)
- 🟡 [Can a Protocol require attributes, not just methods?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-protocol-attributes)
- 🟡 [At what moment does an unimplemented abstract method raise?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-enforcing-abstract-at-runtime)
- 🔴 [Which methods must you implement to get free mixins from `collections.abc`?](https://interview-prep.coderboi.com/python/oop/abc-protocols#q-collections-abc-mixins)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/oop/abc-protocols)

---

## Data Structures

Know the time complexity of each operation. Interviewers will ask why you chose a dict over a list.

### Lists & Slicing

- 🟡 [What is the difference between a Python list and an array?](https://interview-prep.coderboi.com/python/data-structures/lists#q-list-vs-array)
- 🟡 [How does list slicing work, including negative steps?](https://interview-prep.coderboi.com/python/data-structures/lists#q-slicing-semantics)
- 🟡 [What is the difference between append, extend, and insert?](https://interview-prep.coderboi.com/python/data-structures/lists#q-append-extend-insert)
- 🟡 [Are list comprehensions faster than equivalent for loops?](https://interview-prep.coderboi.com/python/data-structures/lists#q-comprehension-vs-loop)
- 🟢 [What is the difference between list.sort() and sorted()?](https://interview-prep.coderboi.com/python/data-structures/lists#q-sort-vs-sorted)
- 🟡 [What is the trap with [[]] * 3?](https://interview-prep.coderboi.com/python/data-structures/lists#q-list-multiplication-trap)
- 🟡 [Why shouldn't you remove items from a list while iterating it?](https://interview-prep.coderboi.com/python/data-structures/lists#q-remove-while-iterating)
- 🟡 [How do you copy a list, and what is shallow vs deep?](https://interview-prep.coderboi.com/python/data-structures/lists#q-shallow-copy-list)
- 🟢 [How does negative indexing work?](https://interview-prep.coderboi.com/python/data-structures/lists#q-negative-index)
- 🟢 [How do you loop with both index and value?](https://interview-prep.coderboi.com/python/data-structures/lists#q-enumerate-list)
- 🟡 [Can you use a list as a stack and a queue?](https://interview-prep.coderboi.com/python/data-structures/lists#q-list-as-stack-queue)
- 🟡 [What is the time complexity of `x in my_list`?](https://interview-prep.coderboi.com/python/data-structures/lists#q-in-operator-list)
- 🟡 [How does starred unpacking work with lists?](https://interview-prep.coderboi.com/python/data-structures/lists#q-list-unpacking-star)
- 🟡 [How do you sort a list of objects by a field?](https://interview-prep.coderboi.com/python/data-structures/lists#q-sort-key-reverse)
- 🔴 [How do you keep a list sorted efficiently as you insert?](https://interview-prep.coderboi.com/python/data-structures/lists#q-bisect-insort)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/data-structures/lists)

### Tuples & Named Tuples

- 🟢 [What is the difference between a tuple and a list, and when should you use each?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-vs-list)
- 🟢 [What are tuple packing and unpacking, and how do you write a single-element tuple?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-packing-unpacking)
- 🟡 [Is a tuple's immutability deep? Can a tuple contain mutable objects?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-shallow-immutability)
- 🟡 [What is a namedtuple and how does collections.namedtuple compare to typing.NamedTuple?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-namedtuple)
- 🟡 [Why can a tuple be used as a dictionary key when a list cannot?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-dict-key)
- 🟢 [Do tuples require parentheses?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-no-parens)
- 🟡 [Are tuples faster or lighter than lists?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-performance)
- 🟢 [What methods do tuples have?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-methods)
- 🟡 [What extra features does a namedtuple add?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-namedtuple-fields)
- 🟡 [When do you choose a namedtuple vs a dataclass?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-vs-dataclass)
- 🟢 [How does tuple unpacking enable swapping without a temp variable?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-unpacking-swap)
- 🟡 [How do *args and tuples relate?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-in-functions)
- 🟡 [What happens when you concatenate or multiply tuples?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-concatenation)
- 🟡 [How are tuples compared?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-comparison)
- 🟢 [Why is (5) not a tuple but (5,) is?](https://interview-prep.coderboi.com/python/data-structures/tuples#q-tuple-single-element)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/data-structures/tuples)

### Dictionaries

- 🟢 [Are Python dictionaries ordered?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-insertion-ordering)
- 🟢 [What is the difference between d[key], d.get(key), and d.setdefault()?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-get-vs-bracket-setdefault)
- 🟡 [What are the ways to merge two dictionaries?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-merging-dicts)
- 🟡 [What do keys(), values(), and items() return, and what is a view object?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-keys-values-items-views)
- 🟡 [Why must dictionary keys be hashable, and why are lookups O(1)?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-keys-hashable-lookup)
- 🟢 [What is a dict comprehension?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-comprehension)
- 🟢 [What are the ways to remove a key from a dict?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-pop-del)
- 🟡 [Can you modify a dict while iterating over it?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-iteration-order)
- 🟡 [When does setdefault shine over get, and what is its catch?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-get-vs-setdefault)
- 🟡 [Why can't you use a list as a dict key but can use a tuple?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-hashable-keys-mutable)
- 🟢 [What does dict.fromkeys do, and what is its shared-default trap?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-comprehension-from-keys)
- 🔴 [How does a Python dict handle hash collisions internally?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-hashmap-collisions)
- 🟡 [Are dict view objects live?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-memory-views-live)
- 🟢 [What do the | and |= dict operators do?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-merge-operator)
- 🟡 [For counting, when do you choose Counter vs defaultdict(int) vs get?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-default-vs-counter)
- 🔴 [How does a dict decide two keys are the same?](https://interview-prep.coderboi.com/python/data-structures/dictionaries#q-dict-key-collision-equality)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/data-structures/dictionaries)

### Sets & Frozensets

- 🟢 [What are the main set operations in Python?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-operations)
- 🟡 [Why is membership testing faster in a set than a list?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-vs-list-membership)
- 🟢 [How do you remove duplicates from a list using a set?](https://interview-prep.coderboi.com/python/data-structures/sets#q-dedup-with-set)
- 🟢 [What is the difference between add, discard, and remove on a set?](https://interview-prep.coderboi.com/python/data-structures/sets#q-add-discard-remove)
- 🟡 [What is a frozenset and when do you need one?](https://interview-prep.coderboi.com/python/data-structures/sets#q-frozenset)
- 🟢 [What is a set comprehension?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-comprehension)
- 🟢 [How do you create an empty set?](https://interview-prep.coderboi.com/python/data-structures/sets#q-empty-set-literal)
- 🟡 [What types can go into a set?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-element-hashable)
- 🟢 [Are sets ordered or indexable?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-unordered)
- 🟡 [How do you test subset and superset relationships?](https://interview-prep.coderboi.com/python/data-structures/sets#q-subset-superset)
- 🟡 [What is the difference between | and |= (and friends) on sets?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-mutating-ops)
- 🟡 [What does symmetric difference do?](https://interview-prep.coderboi.com/python/data-structures/sets#q-symmetric-difference)
- 🟡 [Do sets and frozensets have the same performance?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-vs-frozenset-perf)
- 🟡 [How do you dedupe a list but preserve order?](https://interview-prep.coderboi.com/python/data-structures/sets#q-dedupe-preserve-order)
- 🟡 [What are the complexities of common set operations?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-complexity)
- 🟢 [Is set iteration/copy shallow, and how do you copy a set?](https://interview-prep.coderboi.com/python/data-structures/sets#q-set-copy)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/data-structures/sets)

### The collections Module

- 🟢 [What is collections.Counter and what is it good for?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-counter)
- 🟢 [How does collections.defaultdict work, and how is it different from dict.setdefault?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-defaultdict)
- 🟡 [What is a collections.deque and why use it over a list?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-deque)
- 🟡 [Is OrderedDict still useful now that regular dicts keep insertion order (3.7+)?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-ordereddict)
- 🟡 [What is collections.ChainMap?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-chainmap)
- 🟢 [How does namedtuple fit into the collections module?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-namedtuple-crossref)
- 🟢 [How do you get the N most frequent items with Counter?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-counter-most-common)
- 🟡 [How do Counters support arithmetic?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-counter-arithmetic)
- 🟡 [Can a Counter hold zero or negative counts?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-counter-negative)
- 🟡 [What factory functions are common with defaultdict?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-defaultdict-factory)
- 🟡 [What is a subtle pitfall of defaultdict?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-defaultdict-keyerror-pitfall)
- 🟡 [What does a deque's maxlen do?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-deque-maxlen)
- 🟡 [What does deque.rotate do and what are deque's complexity guarantees?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-deque-rotate)
- 🟡 [Where do writes go in a ChainMap?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-chainmap-updates)
- 🟡 [Does OrderedDict have any methods regular dict lacks?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-ordereddict-still-useful)
- 🔴 [When would you subclass UserDict or UserList instead of dict/list?](https://interview-prep.coderboi.com/python/data-structures/collections-module#q-userdict-userlist)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/data-structures/collections-module)

---

## Iteration

Generators are underrated. Being able to write one from scratch signals real Python fluency.

### Generators & yield

- 🟢 [What is a generator and what does the yield keyword do?](https://interview-prep.coderboi.com/python/iteration/generators#q-what-is-generator)
- 🟡 [How does a generator save memory compared to a list?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-vs-list-memory)
- 🟡 [What is the difference between a generator expression and a list comprehension?](https://interview-prep.coderboi.com/python/iteration/generators#q-genexp-vs-listcomp)
- 🟡 [What does yield from do?](https://interview-prep.coderboi.com/python/iteration/generators#q-yield-from)
- 🔴 [How can a generator be infinite, and why doesn't it hang?](https://interview-prep.coderboi.com/python/iteration/generators#q-infinite-generators)
- 🔴 [What does the generator `send()` method do?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-send)
- 🟡 [What happens when a generator uses `return`?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-return-value)
- 🔴 [What do a generator's `close()` and `throw()` methods do?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-close-throw)
- 🟡 [How do you build a data-processing pipeline with generators?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-pipeline)
- 🟡 [Why can you only iterate a generator once?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-is-iterator)
- 🟡 [How does generator laziness improve responsiveness, not just memory?](https://interview-prep.coderboi.com/python/iteration/generators#q-lazy-evaluation-benefit)
- 🟡 [Why write a generator instead of a class with `__iter__`/`__next__`?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-vs-iterator-class)
- 🔴 [How does a generator preserve local state between `yield`s?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-state-machine)
- 🔴 [How does `yield from` simplify recursive generators?](https://interview-prep.coderboi.com/python/iteration/generators#q-nested-yield-from-tree)
- 🟡 [What's a common bug when passing a generator to multiple functions?](https://interview-prep.coderboi.com/python/iteration/generators#q-generator-exhaustion-pitfall)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/iteration/generators)

### List, Dict & Set Comprehensions

- 🟢 [What is a list comprehension and why use one?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-list-comp-syntax)
- 🟢 [How do you filter and conditionally transform inside a comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-filtering)
- 🟡 [How do nested comprehensions work?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-nested-comp)
- 🟢 [What are dict and set comprehensions?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-dict-set-comp)
- 🟡 [When should you NOT use a comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-vs-map-filter)
- 🟡 [What is a generator expression and how does it differ from a list comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-generator-expression)
- 🟡 [Does the loop variable in a comprehension leak into the enclosing scope?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-scope-leak)
- 🔴 [How is the walrus operator useful inside a comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-walrus-in-comp)
- 🟡 [How do you filter or transform values in a dict comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-conditional-dict-comp)
- 🟡 [Why is a comprehension often faster than an equivalent for-loop?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-performance)
- 🟡 [What is the difference between `[x for row in m for x in row]` and `[[...] for ...]`?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-flatten-vs-nested-output)
- 🟡 [Can a later `for` clause depend on an earlier one in a comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-dependent-nested-loops)
- 🟢 [How do you avoid calling an expensive function twice in a filtered comprehension?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-with-function-call)
- 🟢 [What does a comprehension return when the source is empty?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-empty-and-edge-comp)
- 🟢 [When does a comprehension become too complex and need refactoring?](https://interview-prep.coderboi.com/python/iteration/comprehensions#q-comp-readability-limit)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/iteration/comprehensions)

### Iterators & the Iterator Protocol

- 🟡 [What is the difference between an iterable and an iterator?](https://interview-prep.coderboi.com/python/iteration/iterators#q-iterable-vs-iterator)
- 🟡 [What methods make up the iterator protocol?](https://interview-prep.coderboi.com/python/iteration/iterators#q-iter-next-protocol)
- 🟢 [What do the built-in iter() and next() functions do?](https://interview-prep.coderboi.com/python/iteration/iterators#q-iter-next-builtins)
- 🟡 [How do you build a custom iterator class?](https://interview-prep.coderboi.com/python/iteration/iterators#q-custom-iterator-class)
- 🔴 [How does a for loop work under the hood?](https://interview-prep.coderboi.com/python/iteration/iterators#q-for-under-the-hood)
- 🟡 [Why can you only iterate an iterator once?](https://interview-prep.coderboi.com/python/iteration/iterators#q-iterator-exhaustion)
- 🔴 [What does the two-argument form `iter(callable, sentinel)` do?](https://interview-prep.coderboi.com/python/iteration/iterators#q-iter-sentinel-form)
- 🟡 [How do you make a class that can be iterated multiple times?](https://interview-prep.coderboi.com/python/iteration/iterators#q-reusable-iterable-class)
- 🟡 [How do you slice an iterator without converting it to a list?](https://interview-prep.coderboi.com/python/iteration/iterators#q-itertools-islice)
- 🔴 [How does `itertools.tee` let you iterate a source more than once?](https://interview-prep.coderboi.com/python/iteration/iterators#q-tee-iterator)
- 🟡 [How can you peek at the next value of an iterator without consuming it?](https://interview-prep.coderboi.com/python/iteration/iterators#q-peeking-iterator)
- 🟡 [How do you check whether an iterator is empty?](https://interview-prep.coderboi.com/python/iteration/iterators#q-empty-iterator-check)
- 🟡 [How does the `reversed()` built-in work and what does it require?](https://interview-prep.coderboi.com/python/iteration/iterators#q-reversed-builtin)
- 🔴 [Why shouldn't you let `StopIteration` leak out of a generator?](https://interview-prep.coderboi.com/python/iteration/iterators#q-stopiteration-in-generator)
- 🟢 [Are `map` and `filter` iterators in Python 3?](https://interview-prep.coderboi.com/python/iteration/iterators#q-lazy-map-filter)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/iteration/iterators)

### enumerate, zip & Unpacking

- 🟢 [What does enumerate do and how do you set its start?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-enumerate-basics)
- 🟢 [What does zip do and how does zip_longest differ?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-basics)
- 🟡 [How do you unzip a list of pairs with zip(*)?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-unzip-with-star)
- 🟢 [How does extended (star) unpacking work?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-extended-unpacking)
- 🟡 [How do you build a dict from zip and pass star-args in a call?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-dict-star-args)
- 🟡 [What does `zip(..., strict=True)` do?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-strict)
- 🟢 [Why is `enumerate` preferred over `range(len(seq))`?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-enumerate-vs-range-len)
- 🟡 [How do you combine `zip` with a comprehension for parallel processing?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-with-comprehension)
- 🟡 [How does nested unpacking work in a for loop?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-nested-unpacking)
- 🟡 [Can you mix `*args` unpacking with regular arguments in a call?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-star-in-middle-call)
- 🟡 [How do you use `*` and `**` to merge collections in literals?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-unpacking-in-literals)
- 🟡 [Is `zip` lazy, and what's the consequence?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-is-lazy)
- 🟢 [Does `enumerate` work on generators and other non-sequences?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-enumerate-on-any-iterable)
- 🟢 [How does tuple unpacking enable swapping without a temp variable?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-swap-with-unpacking)
- 🟡 [What's a subtle bug when zipping iterables of unknown length?](https://interview-prep.coderboi.com/python/iteration/enumerate-zip#q-zip-uneven-data-loss)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/iteration/enumerate-zip)

---

## Functional

map/filter/reduce plus itertools — know when to reach for them and when not to.

### functools

- 🟡 [What does functools.lru_cache do?](https://interview-prep.coderboi.com/python/functional/functools#q-lru-cache)
- 🟡 [What is functools.partial used for?](https://interview-prep.coderboi.com/python/functional/functools#q-partial)
- 🟡 [Why do you use functools.wraps when writing a decorator?](https://interview-prep.coderboi.com/python/functional/functools#q-wraps)
- 🟡 [What does functools.reduce do?](https://interview-prep.coderboi.com/python/functional/functools#q-reduce)
- 🔴 [What are cached_property and singledispatch?](https://interview-prep.coderboi.com/python/functional/functools#q-cached-property-singledispatch)
- 🟡 [What is functools.cache and how does it differ from lru_cache?](https://interview-prep.coderboi.com/python/functional/functools#q-cache-vs-lru-cache)
- 🟡 [What are the constraints on lru_cache arguments?](https://interview-prep.coderboi.com/python/functional/functools#q-lru-cache-hashable)
- 🟡 [What does functools.total_ordering do?](https://interview-prep.coderboi.com/python/functional/functools#q-total-ordering)
- 🔴 [What is functools.partialmethod?](https://interview-prep.coderboi.com/python/functional/functools#q-partialmethod)
- 🟡 [Why pass an initializer to functools.reduce?](https://interview-prep.coderboi.com/python/functional/functools#q-reduce-with-initial)
- 🔴 [How do you register implementations with singledispatch?](https://interview-prep.coderboi.com/python/functional/functools#q-singledispatch-register)
- 🟡 [How does cached_property differ from property?](https://interview-prep.coderboi.com/python/functional/functools#q-cached-property-vs-property)
- 🟡 [What exactly does functools.wraps copy?](https://interview-prep.coderboi.com/python/functional/functools#q-wraps-what-it-copies)
- 🟡 [When is functools.partial better than a lambda?](https://interview-prep.coderboi.com/python/functional/functools#q-partial-vs-lambda)
- 🟢 [When should you NOT use reduce?](https://interview-prep.coderboi.com/python/functional/functools#q-reduce-vs-sum)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functional/functools)

### map, filter & reduce

- 🟢 [What does map do and is it lazy?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-map-basics)
- 🟡 [How does map work with multiple iterables?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-map-multiple-iterables)
- 🟢 [What does filter do?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-filter)
- 🟡 [What is functools.reduce and why isn't it a built-in anymore?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-reduce)
- 🟡 [When should you use map/filter versus a comprehension?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-vs-comprehensions)
- 🟡 [Why can a map or filter object only be consumed once?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-consume-once)
- 🟡 [Is map(f, xs) the same as (f(x) for x in xs)?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-map-vs-genexpr)
- 🟡 [How does map with multiple iterables relate to zip?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-map-none-zip)
- 🟢 [What does filter(None, iterable) do?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-filter-none)
- 🟡 [Why do PEP 8 and idiomatic Python often prefer comprehensions?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-comprehension-over-map-filter)
- 🟡 [What is the pitfall of map/filter being lazy?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-lazy-eval-pitfall)
- 🟡 [Why did Guido move reduce out of builtins?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-reduce-readability)
- 🟡 [Should you use map just to call a function for its side effects?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-map-side-effects)
- 🟡 [How do you efficiently chain transformations on a large stream?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-chaining-map-filter)
- 🟡 [When do you need starmap over map?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-starmap-vs-map)
- 🟢 [How do you build a dict from map/zip results?](https://interview-prep.coderboi.com/python/functional/map-filter-reduce#q-dict-from-map)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functional/map-filter-reduce)

### itertools

- 🟡 [What do count, cycle, and repeat do?](https://interview-prep.coderboi.com/python/functional/itertools#q-infinite-iterators)
- 🟢 [What does itertools.chain do?](https://interview-prep.coderboi.com/python/functional/itertools#q-chain)
- 🟡 [What is islice and how is it different from regular slicing?](https://interview-prep.coderboi.com/python/functional/itertools#q-islice)
- 🟡 [What do combinations, permutations, and product produce?](https://interview-prep.coderboi.com/python/functional/itertools#q-combinatorics)
- 🔴 [Why does itertools.groupby require sorted input?](https://interview-prep.coderboi.com/python/functional/itertools#q-groupby)
- 🟡 [What does itertools.accumulate do?](https://interview-prep.coderboi.com/python/functional/itertools#q-accumulate)
- 🟡 [What is the main benefit of itertools being lazy?](https://interview-prep.coderboi.com/python/functional/itertools#q-laziness-memory)
- 🟡 [What is itertools.chain.from_iterable for?](https://interview-prep.coderboi.com/python/functional/itertools#q-chain-from-iterable)
- 🔴 [What does itertools.tee do and what's its catch?](https://interview-prep.coderboi.com/python/functional/itertools#q-tee)
- 🟡 [How does itertools.zip_longest differ from zip?](https://interview-prep.coderboi.com/python/functional/itertools#q-zip-longest)
- 🟡 [What do takewhile and dropwhile do?](https://interview-prep.coderboi.com/python/functional/itertools#q-takewhile-dropwhile)
- 🟡 [When do you use itertools.starmap instead of map?](https://interview-prep.coderboi.com/python/functional/itertools#q-starmap)
- 🟢 [What is itertools.filterfalse?](https://interview-prep.coderboi.com/python/functional/itertools#q-filterfalse)
- 🟡 [What does itertools.pairwise do?](https://interview-prep.coderboi.com/python/functional/itertools#q-pairwise)
- 🟢 [How is itertools.count different from range?](https://interview-prep.coderboi.com/python/functional/itertools#q-count-step)
- 🟡 [How do you correctly consume itertools.groupby output?](https://interview-prep.coderboi.com/python/functional/itertools#q-groupby-pattern)
- 🟡 [Can islice do negative indices or steps?](https://interview-prep.coderboi.com/python/functional/itertools#q-islice-step)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/functional/itertools)

---

## Exceptions

Context managers are a common gotcha. Be ready to write one using both approaches.

### Context Managers & with

- 🟢 [What is a context manager and what does the with statement do?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-what-is-context-manager)
- 🟡 [How do __enter__ and __exit__ work?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-enter-exit)
- 🟡 [How does contextlib.contextmanager simplify writing one?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-contextlib-decorator)
- 🔴 [How does a context manager handle exceptions in __exit__?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-exceptions-in-exit)
- 🟢 [How do you use multiple context managers and what are real uses?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-multiple-context-managers)
- 🔴 [How does __exit__ suppress an exception?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-exit-return-suppress)
- 🟡 [What does contextlib.suppress do?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-contextlib-suppress)
- 🟡 [What is contextlib.closing for?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-contextlib-closing)
- 🟡 [In a @contextmanager generator, why wrap yield in try/finally?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-contextmanager-yield-cleanup)
- 🔴 [What problem does contextlib.ExitStack solve?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-exitstack)
- 🔴 [Can you reuse a context manager instance across multiple with blocks?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-reusable-vs-reentrant)
- 🟡 [What determines the value bound by `as` in a with statement?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-enter-return-value)
- 🔴 [What is an async context manager?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-async-context-manager)
- 🟡 [How do you open several context managers in one with statement?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-nested-vs-parenthesized)
- 🔴 [How do you handle an exception inside a @contextmanager generator?](https://interview-prep.coderboi.com/python/exceptions/context-managers#q-contextmanager-exception-inject)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/exceptions/context-managers)

### try / except / else / finally

- 🟡 [What do the try, except, else, and finally clauses do and when does each run?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-four-clauses)
- 🟡 [How do you catch multiple exception types, and what does `as e` give you?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-catch-multiple)
- 🟡 [Why is a bare `except:` considered bad practice?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-bare-except)
- 🔴 [What happens when `finally` contains a `return`?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-finally-return)
- 🔴 [How do you re-raise an exception and what is exception chaining?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-reraise-chaining)
- 🟡 [What is the point of the else clause on try?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-else-clause-purpose)
- 🔴 [Why is the `as e` variable deleted after the except block?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-exception-as-scope)
- 🟡 [Does the order of except clauses matter?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-exception-order)
- 🟢 [How do you handle several exception types the same way?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-catch-tuple)
- 🟡 [What does `raise X from Y` do?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-raise-from)
- 🟡 [Are exceptions expensive in Python?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-exception-cost)
- 🔴 [What happens when both try and finally return?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-try-finally-return-override)
- 🟡 [How does exception propagation work through nested try blocks?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-nested-try)
- 🟡 [When should you use assert instead of raising an exception?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-assert-vs-raise)
- 🟡 [How do you log an exception with its traceback?](https://interview-prep.coderboi.com/python/exceptions/try-except#q-logging-exceptions)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/exceptions/try-except)

### Custom Exceptions & the Hierarchy

- 🟡 [What is the Python exception hierarchy and why shouldn't you catch BaseException?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-hierarchy)
- 🟢 [How do you define a custom exception class?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-defining-custom)
- 🟡 [When and why should you create custom exceptions?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-when-to-subclass)
- 🟡 [How do you pass arguments and messages to an exception?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-passing-args)
- 🟡 [Why does catching a base exception class also catch its subclasses?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-base-catches-subclasses)
- 🟢 [What are some common built-in exceptions and when are they raised?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-common-builtins)
- 🟡 [Why inherit from Exception and not BaseException?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-exception-vs-baseexception)
- 🟡 [How does the args attribute and str() of an exception work?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-exception-args)
- 🔴 [What are ExceptionGroup and except* (3.11+)?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-exception-group)
- 🟡 [Why catch specific exceptions rather than broad ones?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-catch-specific)
- 🟡 [How do you re-raise an exception without losing the traceback?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-reraise-preserve-traceback)
- 🟡 [What is the EAFP pattern with exceptions?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-exception-with-cleanup-pattern)
- 🟡 [How do you attach structured data to a custom exception?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-custom-exception-attributes)
- 🟡 [How do you design an exception hierarchy for a library?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-exception-hierarchy-design)
- 🟡 [When does finally NOT run?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-finally-cleanup-guarantee)
- 🟡 [When do you use warnings instead of exceptions?](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions#q-warnings-vs-exceptions)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/exceptions/custom-exceptions)

---

## Concurrency

The GIL is the question everyone asks about Python concurrency. Know it cold — what it is, what it doesn't protect, and when multiprocessing is the answer.

### Threading & the GIL

- 🔴 [What is the GIL?](https://interview-prep.coderboi.com/python/concurrency/gil#q-what-is-the-gil)
- 🟡 [What is the difference between threading and multiprocessing?](https://interview-prep.coderboi.com/python/concurrency/gil#q-threading-vs-multiprocessing)
- 🔴 [Why don't threads speed up CPU-bound work but help I/O-bound work?](https://interview-prep.coderboi.com/python/concurrency/gil#q-cpu-vs-io-bound)
- 🔴 [What is a race condition and how do locks prevent it?](https://interview-prep.coderboi.com/python/concurrency/gil#q-race-conditions-locks)
- 🟡 [When do you use ThreadPoolExecutor vs ProcessPoolExecutor?](https://interview-prep.coderboi.com/python/concurrency/gil#q-threadpool-vs-processpool)
- 🟡 [Why does CPython have a GIL at all?](https://interview-prep.coderboi.com/python/concurrency/gil#q-why-gil-exists)
- 🔴 [When does the GIL get released?](https://interview-prep.coderboi.com/python/concurrency/gil#q-gil-release)
- 🔴 [Is the GIL going away?](https://interview-prep.coderboi.com/python/concurrency/gil#q-gil-310-free-threading)
- 🟡 [What is the difference between Lock and RLock?](https://interview-prep.coderboi.com/python/concurrency/gil#q-lock-vs-rlock)
- 🔴 [What causes a deadlock and how do you avoid it?](https://interview-prep.coderboi.com/python/concurrency/gil#q-deadlock)
- 🟡 [Are Python's built-in data structures thread-safe?](https://interview-prep.coderboi.com/python/concurrency/gil#q-thread-safe-structures)
- 🟡 [What is a daemon thread?](https://interview-prep.coderboi.com/python/concurrency/gil#q-daemon-threads)
- 🟡 [What does thread.join do?](https://interview-prep.coderboi.com/python/concurrency/gil#q-join-threads)
- 🟡 [What is threading.local used for?](https://interview-prep.coderboi.com/python/concurrency/gil#q-threadlocal)
- 🟡 [Does the GIL make Python code automatically thread-safe?](https://interview-prep.coderboi.com/python/concurrency/gil#q-gil-misconception)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/concurrency/gil)

### Multiprocessing

- 🔴 [How does multiprocessing sidestep the GIL, and how is it different from threading?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-multiprocessing-vs-threading)
- 🟡 [What is the difference between Process and Pool?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-process-vs-pool)
- 🔴 [How do processes communicate (Queue vs Pipe)?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-ipc-queue-pipe)
- 🔴 [What is the pickling overhead, and what can't be pickled?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-pickling-overhead)
- 🔴 [How do you share state between processes?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-shared-state)
- 🟡 [When should you use multiprocessing instead of threads or asyncio?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-when-multiprocessing)
- 🟡 [Why is `if __name__ == "__main__"` required with multiprocessing?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-main-guard)
- 🔴 [What are the spawn, fork, and forkserver start methods?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-start-methods)
- 🟡 [What is the difference between Pool.map, imap, and apply_async?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-pool-map-variants)
- 🔴 [What does multiprocessing.shared_memory offer over Queue/Pipe?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-shared-memory-class)
- 🟡 [How does multiprocessing.Pool differ from ProcessPoolExecutor?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-pool-vs-processpoolexecutor)
- 🟡 [What is a multiprocessing.Manager?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-manager)
- 🟡 [How do Value and Array share state between processes?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-value-array)
- 🟡 [What happens if you don't join child processes?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-zombie-join)
- 🟡 [What is the overhead of multiprocessing?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-process-overhead)
- 🔴 [Why can Ctrl-C behave oddly with multiprocessing pools?](https://interview-prep.coderboi.com/python/concurrency/multiprocessing#q-keyboardinterrupt-pool)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/concurrency/multiprocessing)

### asyncio & async/await

- 🔴 [What is asyncio and the event loop?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-what-is-asyncio)
- 🟡 [What do async def and await do?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-async-def-await)
- 🔴 [How do coroutines differ from threads?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-coroutines-vs-threads)
- 🟡 [How do you run coroutines concurrently with asyncio.gather?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-asyncio-gather)
- 🔴 [What is the "don't block the event loop" rule?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-dont-block-the-loop)
- 🟡 [When does asyncio actually help?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-when-async-helps)
- 🟡 [What is the difference between awaiting a coroutine and asyncio.create_task?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-create-task)
- 🟡 [What is the difference between asyncio.gather and asyncio.wait?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-gather-vs-wait)
- 🟡 [How does gather behave when a task raises, and what does return_exceptions do?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-return-exceptions)
- 🟡 [How do you call blocking code from async without freezing the loop?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-to-thread)
- 🟡 [How do you put a timeout on an awaitable?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-timeout)
- 🔴 [How does task cancellation work in asyncio?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-cancellation)
- 🟡 [What are async with and async for used for?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-async-with-for)
- 🟡 [How do you limit how many coroutines run at once?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-semaphore)
- 🟡 [What is asyncio.Queue used for?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-asyncio-queue)
- 🔴 [Why does "asyncio.run() cannot be called from a running event loop" happen?](https://interview-prep.coderboi.com/python/concurrency/asyncio#q-loop-already-running)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/concurrency/asyncio)

### concurrent.futures

- 🟡 [What is the Executor abstraction in concurrent.futures?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-executor-abstraction)
- 🟡 [When do you use ThreadPoolExecutor vs ProcessPoolExecutor?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-thread-vs-process-pool)
- 🟡 [What does submit() return, and what is a Future?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-submit-and-futures)
- 🟢 [How does executor.map work and how does it differ from submit?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-executor-map)
- 🟡 [What does as_completed do?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-as-completed)
- 🟡 [How are exceptions handled with futures?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-exception-propagation)
- 🟡 [Why use an Executor as a context manager?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-with-statement-shutdown)
- 🟡 [What is the default max_workers for the executors?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-max-workers-default)
- 🟡 [What do the timeout and chunksize arguments to map do?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-map-timeout-chunksize)
- 🟡 [Can you cancel a submitted future?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-cancel-future)
- 🟡 [What does add_done_callback do?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-add-done-callback)
- 🔴 [How does concurrent.futures relate to asyncio?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-futures-vs-asyncio)
- 🔴 [What concurrency pitfall comes from submitting to a pool from within a pool task?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-deadlock-nested-pools)
- 🟡 [What is the initializer argument used for?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-initializer)
- 🟡 [What does the return_when argument of concurrent.futures.wait do?](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures#q-wait-returnwhen)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/concurrency/concurrent-futures)

---

## Modules

Import mechanics and virtual environments are basic, but getting them wrong sends a bad signal.

### The Import System

- 🟢 [What is the difference between a module and a package?](https://interview-prep.coderboi.com/python/modules/imports#q-module-vs-package)
- 🟡 [What is the difference between absolute and relative imports?](https://interview-prep.coderboi.com/python/modules/imports#q-absolute-vs-relative-imports)
- 🟢 [What does `if __name__ == "__main__"` do?](https://interview-prep.coderboi.com/python/modules/imports#q-name-main)
- 🟡 [How does Python find the module you import?](https://interview-prep.coderboi.com/python/modules/imports#q-sys-path-resolution)
- 🔴 [What is `sys.modules` and how does it relate to circular imports?](https://interview-prep.coderboi.com/python/modules/imports#q-import-caching-circular)
- 🟡 [What does `from module import *` do and how does `__all__` control it?](https://interview-prep.coderboi.com/python/modules/imports#q-import-star-and-all)
- 🟢 [What's the practical difference between `import x` and `from x import y`?](https://interview-prep.coderboi.com/python/modules/imports#q-import-vs-from-import)
- 🟡 [Why and how would you import a module lazily inside a function?](https://interview-prep.coderboi.com/python/modules/imports#q-lazy-import)
- 🔴 [How do you reload a module, and why is it rarely the right tool?](https://interview-prep.coderboi.com/python/modules/imports#q-reload-module)
- 🟡 [What is the role of `__init__.py` in a package?](https://interview-prep.coderboi.com/python/modules/imports#q-package-init-role)
- 🟡 [How do you handle an optional dependency with try/except imports?](https://interview-prep.coderboi.com/python/modules/imports#q-conditional-import-fallback)
- 🟡 [What does `python -m package` do and why use it?](https://interview-prep.coderboi.com/python/modules/imports#q-running-package-m)
- 🔴 [What is a namespace package and when is it useful?](https://interview-prep.coderboi.com/python/modules/imports#q-namespace-packages)
- 🟢 [What useful attributes does a module object have?](https://interview-prep.coderboi.com/python/modules/imports#q-module-attributes)
- 🟡 [What is the `__pycache__` directory and the `.pyc` files in it?](https://interview-prep.coderboi.com/python/modules/imports#q-pycache-bytecode)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/modules/imports)

### Packages & __main__

- 🟢 [What is the difference between a module and a package, and what does __init__.py do?](https://interview-prep.coderboi.com/python/modules/packages#q-package-vs-module)
- 🟡 [What do `python -m` and __main__.py do?](https://interview-prep.coderboi.com/python/modules/packages#q-python-m-main)
- 🟡 [What does __all__ control?](https://interview-prep.coderboi.com/python/modules/packages#q-dunder-all)
- 🔴 [What is a namespace package?](https://interview-prep.coderboi.com/python/modules/packages#q-namespace-packages)
- 🟡 [What is the difference between running a file and importing it?](https://interview-prep.coderboi.com/python/modules/packages#q-script-vs-import)
- 🟡 [What's the difference between an import package and a distribution package?](https://interview-prep.coderboi.com/python/modules/packages#q-import-package-vs-distribution)
- 🟡 [What is `pyproject.toml` and why did it replace `setup.py`?](https://interview-prep.coderboi.com/python/modules/packages#q-pyproject-toml)
- 🟡 [What does `pip install -e .` (editable install) do?](https://interview-prep.coderboi.com/python/modules/packages#q-editable-install)
- 🔴 [How do you expose a command-line tool from a package?](https://interview-prep.coderboi.com/python/modules/packages#q-entry-points-console-scripts)
- 🟡 [How do you access non-code files bundled in a package?](https://interview-prep.coderboi.com/python/modules/packages#q-package-data)
- 🟡 [When do relative imports work and when do they fail?](https://interview-prep.coderboi.com/python/modules/packages#q-relative-import-in-package)
- 🟢 [How do nested subpackages and their imports work?](https://interview-prep.coderboi.com/python/modules/packages#q-subpackage-structure)
- 🔴 [What does a module-level `__getattr__` enable?](https://interview-prep.coderboi.com/python/modules/packages#q-module-level-getattr)
- 🟡 [How do you use `__init__.py` to flatten a package's public API?](https://interview-prep.coderboi.com/python/modules/packages#q-init-reexport-api)
- 🔴 [How does package structure contribute to circular imports?](https://interview-prep.coderboi.com/python/modules/packages#q-circular-import-package)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/modules/packages)

### Virtual Environments & pip

- 🟢 [What is a virtual environment and why does isolation matter?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-what-is-venv)
- 🟢 [How do you create and activate a virtual environment?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-create-activate)
- 🟢 [How do you install packages and what is requirements.txt?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-pip-requirements)
- 🟡 [What does pip freeze do?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-pip-freeze)
- 🟡 [What is an editable install (`pip install -e`)?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-editable-install)
- 🟡 [What is pyproject.toml?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-pyproject-toml)
- 🟡 [How does activating a venv actually change your shell?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-how-venv-works)
- 🟡 [How do `venv`, `virtualenv`, and `conda` differ?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-venv-vs-virtualenv-conda)
- 🟡 [What do version specifiers like `==`, `>=`, `~=` mean in pip?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-version-specifiers)
- 🟡 [When should you use `pipx` instead of `pip`?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-pip-vs-pipx)
- 🔴 [What does pip's dependency resolver do, and what are lock files for?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-dependency-resolution)
- 🟢 [Why should you avoid `sudo pip install`?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-no-sudo-pip)
- 🟢 [How do you upgrade or remove packages with pip?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-upgrade-and-uninstall)
- 🟡 [When do you use `requirements.txt` versus declaring deps in `pyproject.toml`?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-requirements-vs-pyproject)
- 🟢 [What is the pip cache and how do you do offline installs?](https://interview-prep.coderboi.com/python/modules/virtual-environments#q-pip-cache-and-offline)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/modules/virtual-environments)

---

## Typing

Type hints are increasingly expected. Generics and Protocols are the tricky parts.

### Type Hints & Annotations

- 🟢 [Are type hints enforced at runtime?](https://interview-prep.coderboi.com/python/typing/type-hints#q-hints-runtime-enforced)
- 🟡 [What is the difference between Optional, Union, and the `|` operator?](https://interview-prep.coderboi.com/python/typing/type-hints#q-optional-union)
- 🟡 [What is the difference between `list` and `List`, and how do generics work?](https://interview-prep.coderboi.com/python/typing/type-hints#q-list-vs-generics)
- 🔴 [What is the difference between `typing.Any` and `object`?](https://interview-prep.coderboi.com/python/typing/type-hints#q-any-vs-object)
- 🟡 [What does mypy do, and how is it different from Protocol-based typing?](https://interview-prep.coderboi.com/python/typing/type-hints#q-what-mypy-does)
- 🟡 [How do you annotate a function or callable parameter?](https://interview-prep.coderboi.com/python/typing/type-hints#q-callable-annotation)
- 🟡 [How do you create a type alias?](https://interview-prep.coderboi.com/python/typing/type-hints#q-type-aliases)
- 🟡 [What's the difference between annotating with `MyClass` and `type[MyClass]`?](https://interview-prep.coderboi.com/python/typing/type-hints#q-type-vs-instance-annotation)
- 🔴 [What do `Literal` and `Final` express?](https://interview-prep.coderboi.com/python/typing/type-hints#q-literal-final)
- 🔴 [What is `TypedDict` and when do you use it?](https://interview-prep.coderboi.com/python/typing/type-hints#q-typeddict)
- 🟡 [How do you annotate a method that returns its own class?](https://interview-prep.coderboi.com/python/typing/type-hints#q-annotating-self-class)
- 🔴 [What are forward references and `from __future__ import annotations`?](https://interview-prep.coderboi.com/python/typing/type-hints#q-forward-references)
- 🟡 [How do you annotate `*args` and `**kwargs`?](https://interview-prep.coderboi.com/python/typing/type-hints#q-annotating-args-kwargs)
- 🟢 [How do you annotate functions that return nothing or never return?](https://interview-prep.coderboi.com/python/typing/type-hints#q-none-return-annotation)
- 🟡 [What is gradual typing and how do you adopt hints incrementally?](https://interview-prep.coderboi.com/python/typing/type-hints#q-gradual-typing)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/typing/type-hints)

### Generics & Protocols

- 🔴 [What are TypeVar and Generic, and how do you write a generic class?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-typevar-generic)
- 🔴 [What is a bounded or constrained TypeVar?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-bounded-typevar)
- 🔴 [What is typing.Protocol and how does it enable structural typing?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-protocol-structural)
- 🟡 [What does @runtime_checkable do for a Protocol?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-runtime-checkable)
- 🟡 [How do you type a function passed as an argument?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-callable-types)
- 🔴 [What is the difference between covariance and invariance in generics?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-covariance-invariance)
- 🟡 [How do you use multiple type variables in one function or class?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-multiple-typevars)
- 🟡 [What is typing.Self and when is it useful?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-self-type)
- 🔴 [What does @typing.overload do?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-overload)
- 🔴 [What problem does ParamSpec solve?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-paramspec)
- 🔴 [How do you write a generic Protocol?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-generic-protocol)
- 🟡 [Can a Protocol declare attributes, not just methods?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-protocol-attributes)
- 🔴 [How do you declare a covariant or contravariant TypeVar?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-declaring-variance)
- 🟡 [What is the PEP 695 type-parameter syntax in Python 3.12?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-pep695-syntax)
- 🟡 [When should you use a Protocol versus an abstract base class?](https://interview-prep.coderboi.com/python/typing/generics-protocols#q-abc-vs-protocol)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/typing/generics-protocols)

---

## Standard Library

datetime, pathlib, json/pickle — know the standard tools before reaching for third-party libs.

### Regular Expressions

- 🟢 [What is the difference between re.match, re.search, and re.fullmatch?](https://interview-prep.coderboi.com/python/stdlib/regex#q-match-search-fullmatch)
- 🟡 [How do capture groups and named groups work?](https://interview-prep.coderboi.com/python/stdlib/regex#q-groups-named-groups)
- 🟡 [What does re.compile do, and why would you use it?](https://interview-prep.coderboi.com/python/stdlib/regex#q-re-compile-why)
- 🔴 [What is the difference between greedy and non-greedy matching?](https://interview-prep.coderboi.com/python/stdlib/regex#q-greedy-vs-lazy)
- 🟡 [How does re.sub work, and why use raw strings for patterns?](https://interview-prep.coderboi.com/python/stdlib/regex#q-re-sub-raw-strings)
- 🟡 [What is the difference between `findall` and `finditer`?](https://interview-prep.coderboi.com/python/stdlib/regex#q-findall-vs-finditer)
- 🟡 [What do the common regex flags do (IGNORECASE, MULTILINE, DOTALL, VERBOSE)?](https://interview-prep.coderboi.com/python/stdlib/regex#q-common-flags)
- 🟡 [What do `^`, `$`, `\b`, and `\B` anchor?](https://interview-prep.coderboi.com/python/stdlib/regex#q-anchors-boundaries)
- 🔴 [How do backreferences work in a pattern?](https://interview-prep.coderboi.com/python/stdlib/regex#q-backreferences)
- 🟡 [How does `re.split` differ from `str.split`?](https://interview-prep.coderboi.com/python/stdlib/regex#q-split-with-regex)
- 🔴 [What is catastrophic backtracking and how do you avoid it?](https://interview-prep.coderboi.com/python/stdlib/regex#q-catastrophic-backtracking)
- 🔴 [What are lookahead and lookbehind assertions?](https://interview-prep.coderboi.com/python/stdlib/regex#q-lookahead-lookbehind)
- 🟢 [What information does a Match object provide?](https://interview-prep.coderboi.com/python/stdlib/regex#q-match-object-methods)
- 🟡 [How do you limit replacements or count them with `re.sub`?](https://interview-prep.coderboi.com/python/stdlib/regex#q-sub-count-and-subn)
- 🟡 [How do you match a literal string that may contain regex metacharacters?](https://interview-prep.coderboi.com/python/stdlib/regex#q-escaping-special-chars)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/stdlib/regex)

### Files, pathlib & os

- 🟢 [Why open files with the `with` statement?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-with-open)
- 🟡 [What is the difference between iterating a file and read()/readlines()?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-lazy-iteration)
- 🟡 [What is the difference between text and binary mode, and why specify encoding?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-text-binary-mode)
- 🟡 [What is pathlib.Path and how does it compare to os.path?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-pathlib-vs-os-path)
- 🟡 [How do you find files with globbing using pathlib?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-globbing-path-methods)
- 🟢 [What do the file modes `r`, `w`, `a`, `x`, and `+` mean?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-file-modes)
- 🟢 [What are the key parts of a `Path` (name, stem, suffix, parent)?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-path-properties)
- 🟡 [How do you resolve, and work with relative vs absolute paths?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-relative-absolute-paths)
- 🟢 [What are `Path.read_text`, `write_text`, and their bytes variants?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-reading-writing-helpers)
- 🟡 [How do common `os`/`shutil` operations map to `pathlib`?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-os-vs-pathlib-operations)
- 🟡 [How do you safely create temporary files and directories?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-tempfile-usage)
- 🟡 [What do `seek()` and `tell()` do on a file object?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-file-seek-tell)
- 🟡 [What's the difference between glob wildcards `*`, `**`, `?`, and `[...]`?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-glob-vs-pattern-syntax)
- 🔴 [Why might written data not appear in a file immediately?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-file-buffering-flush)
- 🟡 [How do you handle decoding errors when reading text files?](https://interview-prep.coderboi.com/python/stdlib/files-pathlib#q-encoding-errors-handling)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/stdlib/files-pathlib)

### datetime

- 🟢 [What is the difference between datetime, date, and time?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-datetime-date-time)
- 🔴 [What is the difference between naive and timezone-aware datetimes?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-naive-aware-zoneinfo)
- 🟡 [What is the difference between strftime and strptime?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-strftime-strptime)
- 🟡 [How does timedelta arithmetic work?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-timedelta-arithmetic)
- 🔴 [What is the pitfall with datetime.now() vs utcnow()?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-now-vs-utcnow)
- 🟢 [How do you parse and produce ISO 8601 datetime strings?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-fromisoformat)
- 🟡 [How do you convert between datetimes and Unix timestamps?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-timestamp-epoch)
- 🔴 [How does `zoneinfo` handle Daylight Saving Time transitions?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-dst-handling)
- 🟡 [What are the most common `strftime`/`strptime` format codes?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-date-parsing-formats)
- 🟡 [Why are datetime objects immutable and how do you "modify" one?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-replace-and-immutability)
- 🟡 [What's the modern replacement for `datetime.utcnow()`?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-utc-now-modern)
- 🟢 [How do you compare and sort datetimes?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-comparing-sorting-dates)
- 🟡 [When do you use the `time` module instead of `datetime`?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-time-module-vs-datetime)
- 🟢 [How do you get the weekday or work with calendar info?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-calendar-and-weekday)
- 🔴 [How do you parse a string into a timezone-aware datetime?](https://interview-prep.coderboi.com/python/stdlib/datetime#q-parsing-timezone-aware)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/stdlib/datetime)

### JSON, CSV & pickle

- 🟢 [How do json.dumps and json.loads work, and how do Python types map to JSON?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-json-dumps-loads)
- 🟡 [How do you serialize an object JSON doesn't support by default?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-json-custom-encoding)
- 🟡 [What is the difference between csv.reader and csv.DictReader?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-csv-reader-dictreader)
- 🟡 [What is the difference between pickle and json, and what is the security warning?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-pickle-vs-json)
- 🟡 [How do you serialize datetimes to JSON and back?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-serializing-datetimes)
- 🟢 [What options control JSON output formatting?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-json-formatting-options)
- 🟡 [How does `object_hook` reconstruct custom types when loading JSON?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-object-hook-decoding)
- 🟡 [How do you write CSV files correctly?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-csv-writing)
- 🔴 [What happens to special floats and big numbers in JSON?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-json-numeric-precision)
- 🟡 [What are pickle protocols and what can't be pickled?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-pickle-protocols)
- 🟡 [What are safer alternatives to pickle for persistence?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-safe-alternatives-pickle)
- 🟡 [What happens to non-string dict keys when serializing to JSON?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-json-key-coercion)
- 🟡 [How do you handle non-comma delimiters and quoting in CSV?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-csv-dialects-delimiters)
- 🔴 [How do you handle JSON files too large to fit in memory?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-streaming-large-json)
- 🟡 [How do you serialize a dataclass to JSON and back?](https://interview-prep.coderboi.com/python/stdlib/serialization#q-dataclass-json-roundtrip)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/stdlib/serialization)

---

## Internals

CPython internals questions are common at companies that care about Python performance. Know reference counting and what the GC actually handles.

### Garbage Collection & Reference Counting

- 🟡 [How does reference counting work in Python?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-reference-counting)
- 🔴 [Why does Python need a cyclic garbage collector?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-cyclic-gc)
- 🟡 [What does sys.getrefcount tell you and why is it always higher than expected?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-sys-getrefcount)
- 🔴 [What is a weak reference and when do you use one?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-weak-references)
- 🔴 [What are the pitfalls of the __del__ method?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-del-pitfalls)
- 🔴 [What is generational garbage collection?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-generational-gc)
- 🟡 [When might you disable the garbage collector?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-gc-disable-performance)
- 🔴 [Which objects does the cyclic collector track, and which does it ignore?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-container-vs-atomic-tracking)
- 🔴 [How do reference-counting bugs manifest in C extensions?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-refcount-cextension-bugs)
- 🟡 [How can you debug memory leaks with the `gc` module?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-gc-callbacks-debug)
- 🟡 [What is `tracemalloc` used for?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-tracemalloc)
- 🟡 [Why does a small Python object use far more memory than its raw value?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-object-overhead)
- 🟡 [What exactly does the `del` statement do?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-del-statement-vs-method)
- 🔴 [How can a weakref notify you when its referent dies?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-weakref-callback)
- 🔴 [Why might freeing objects not return memory to the operating system?](https://interview-prep.coderboi.com/python/internals/garbage-collection#q-memory-not-returned-os)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/internals/garbage-collection)

### Identity, is vs ==, & Interning

- 🟡 [What is the difference between is and ==?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-is-vs-equals)
- 🟡 [What does the id() function tell you?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-id-function)
- 🟡 [What is the small-int cache?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-small-int-cache)
- 🟡 [What is string interning and sys.intern?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-string-interning)
- 🔴 [Why does is sometimes "work" coincidentally?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-is-coincidental)
- 🟢 [What is the correct use of is?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-correct-use-of-is)
- 🔴 [How do identity and equality relate to hashing in dicts/sets?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-hash-and-identity)
- 🟡 [Can an object's `id()` change during its lifetime?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-mutable-identity-stability)
- 🟡 [Why are `None`, `True`, and `False` always safe to compare with `is`?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-interning-bool-none)
- 🔴 [Why might `a is b` be True for some tuple/string literals in the same line?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-tuple-interning-quirk)
- 🟡 [When is `sys.intern` actually worth using?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-intern-performance-use)
- 🔴 [Why should a custom `__eq__` usually agree with identity for the same object?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-equality-reflexivity)
- 🟡 [How do `copy`, slicing, and assignment differ in identity?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-copy-and-identity)
- 🟡 [What other cached singletons exist besides small ints?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-frozen-singletons)
- 🟢 [How can `id()` help diagnose an aliasing bug?](https://interview-prep.coderboi.com/python/internals/identity-interning#q-id-debugging-aliasing)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/internals/identity-interning)

### The CPython Execution Model

- 🔴 [How does CPython go from source to running code?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-source-to-bytecode)
- 🔴 [What is CPython, and how does it differ from PyPy and Jython?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-cpython-vs-others)
- 🟡 [How do you inspect bytecode with the dis module?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-dis-module)
- 🔴 [What are frames and the call stack?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-frames-call-stack)
- 🟡 [Is Python compiled or interpreted?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-compiled-or-interpreted)
- 🔴 [What role does the GIL play in CPython's execution model?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-gil-role)
- 🔴 [What is a code object and how does it relate to a function?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-code-object)
- 🟡 [How does CPython decide whether to reuse a `.pyc` file?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-pyc-invalidation)
- 🔴 [What compile-time optimizations does CPython apply?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-peephole-optimizer)
- 🔴 [What did the 3.11+ "specializing adaptive interpreter" change?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-specializing-interpreter)
- 🟡 [Why is CPython called a "stack-based" virtual machine?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-stack-based-vm)
- 🟡 [How does CPython resolve a name at the bytecode level?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-globals-builtins-lookup)
- 🟡 [Why does Python have a recursion limit, and how do you change it?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-recursion-limit)
- 🔴 [Does CPython optimize tail recursion?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-no-tail-call)
- 🟡 [What constants does the compiler deduplicate within a code object?](https://interview-prep.coderboi.com/python/internals/cpython-model#q-interning-compile-time)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/internals/cpython-model)

---

## Idioms

EAFP vs LBYL, common gotchas with mutable defaults — the questions that separate experienced Python devs.

### EAFP vs LBYL

- 🟢 [What do EAFP and LBYL mean?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-eafp-lbyl-meaning)
- 🟡 [Why is EAFP preferred in Python?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-why-eafp-preferred)
- 🔴 [What race condition does LBYL invite?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-lbyl-race-condition)
- 🟡 [When should you use dict.get versus checking for a key?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-dict-get-vs-check)
- 🔴 [What are the pitfalls of EAFP, and how do you avoid them?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-eafp-pitfalls)
- 🟡 [When is LBYL actually the better choice?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-when-lbyl-better)
- 🟡 [How does `getattr` with a default express EAFP for attributes?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-getattr-eafp)
- 🟡 [How does `contextlib.suppress` clean up EAFP code?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-contextlib-suppress)
- 🟡 [How does EAFP support duck typing better than type checks?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-eafp-duck-typing)
- 🔴 [Is EAFP or LBYL faster?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-eafp-performance)
- 🟡 [How does the `try/except/else` clause refine EAFP?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-else-clause-eafp)
- 🟡 [When is `defaultdict` better than `dict.get` for accumulation?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-defaultdict-vs-get)
- 🟡 [Why does EAFP depend on catching the right specific exception?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-specific-exception-eafp)
- 🟡 [Where should LBYL-style validation live in an application?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-validation-at-boundaries)
- 🔴 [How can the walrus operator support concise EAFP-style loops?](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl#q-walrus-eafp-loop)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/idioms/eafp-lbyl)

### PEP 8 & Style

- 🟢 [What is PEP 8?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-what-is-pep8)
- 🟢 [What are PEP 8's naming conventions?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-naming-conventions)
- 🟢 [What does PEP 8 say about imports and line length?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-imports-line-length)
- 🟢 [What is the Zen of Python?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-zen-of-python)
- 🟢 [What are black and ruff, and how do formatters differ from linters?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-formatters-linters)
- 🟡 [When is it acceptable to break PEP 8?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-when-break-pep8)
- 🟢 [What are PEP 8's key whitespace rules?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-whitespace-rules)
- 🟢 [How many blank lines does PEP 8 recommend between definitions?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-blank-lines)
- 🟡 [What does PEP 257 say about docstrings?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-docstring-conventions)
- 🟢 [What does PEP 8 recommend for comparisons to None and booleans?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-comparison-style)
- 🟡 [How should you break long lines in PEP 8 style?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-line-continuation)
- 🟡 [What are the PEP 8 spacing rules for type annotations?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-type-hints-style)
- 🟡 [What's the difference between `_name`, `__name`, and `__name__` conventions?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-dunder-naming)
- 🟢 [What small formatting details does PEP 8 require at line and file level?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-trailing-whitespace-eof)
- 🟢 [Does PEP 8 mandate single or double quotes?](https://interview-prep.coderboi.com/python/idioms/pep8-style#q-string-quote-consistency)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/idioms/pep8-style)

### Common Gotchas & Anti-patterns

- 🔴 [Why is a mutable default argument a gotcha?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-mutable-default-arg)
- 🔴 [What is the late-binding closure gotcha in loops?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-late-binding-closures)
- 🟡 [What goes wrong when you modify a list while iterating it?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-modify-while-iterating)
- 🟡 [Why does `is` give surprising results on numbers and strings?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-is-vs-eq-cached)
- 🟡 [Why is a bare except an anti-pattern?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-bare-except)
- 🔴 [Why is a mutable class attribute a common bug?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-mutable-class-attr)
- 🟢 [What is the problem with shadowing builtins?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-shadowing-builtins)
- 🟡 [Why does `0.1 + 0.2 == 0.3` return False?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-integer-float-equality)
- 🔴 [Why does `a += b` behave differently for lists than `a = a + b`?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-chained-augmented-assignment)
- 🟡 [What's wrong with `dict.fromkeys(keys, [])`?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-default-mutable-in-dict)
- 🟡 [Why can `if not value:` be a subtle bug?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-truthiness-empty-check-bug)
- 🟡 [Why is building a string with `+=` in a loop a performance gotcha?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-string-concatenation-loop)
- 🟡 [Why does copying a list with `=` not actually copy it?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-copy-vs-reference)
- 🟡 [Why doesn't a default like `time.time()` update on each call?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-default-argument-evaluation-time)
- 🟢 [Why is `(1)` not a tuple?](https://interview-prep.coderboi.com/python/idioms/gotchas#q-tuple-single-element)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/idioms/gotchas)

---

## Testing

pytest fixtures and mocking are table stakes. Know how to mock correctly (and when not to).

### pytest Essentials

- 🟢 [What is the difference between pytest and unittest?](https://interview-prep.coderboi.com/python/testing/pytest#q-pytest-vs-unittest)
- 🟡 [What are pytest fixtures, and what does scope control?](https://interview-prep.coderboi.com/python/testing/pytest#q-fixtures-scope)
- 🟡 [How does @pytest.mark.parametrize work?](https://interview-prep.coderboi.com/python/testing/pytest#q-parametrize)
- 🔴 [How do you mock with monkeypatch versus unittest.mock?](https://interview-prep.coderboi.com/python/testing/pytest#q-mocking-monkeypatch)
- 🟡 [How do you assert that code raises an exception?](https://interview-prep.coderboi.com/python/testing/pytest#q-pytest-raises)
- 🟡 [What is conftest.py used for?](https://interview-prep.coderboi.com/python/testing/pytest#q-conftest)
- 🟡 [How do you do setup and teardown in a pytest fixture?](https://interview-prep.coderboi.com/python/testing/pytest#q-fixture-yield-teardown)
- 🟢 [What are some useful built-in pytest fixtures?](https://interview-prep.coderboi.com/python/testing/pytest#q-builtin-fixtures)
- 🟡 [What do `skip`, `skipif`, and `xfail` markers do?](https://interview-prep.coderboi.com/python/testing/pytest#q-markers-skip-xfail)
- 🔴 [How do you give parametrized cases readable IDs or parametrize a fixture?](https://interview-prep.coderboi.com/python/testing/pytest#q-parametrize-ids-fixtures)
- 🟡 [How can fixtures depend on other fixtures?](https://interview-prep.coderboi.com/python/testing/pytest#q-fixture-dependencies)
- 🟡 [How does pytest give detailed output from a plain `assert`?](https://interview-prep.coderboi.com/python/testing/pytest#q-assert-introspection)
- 🟢 [How do you assert floating-point equality in pytest?](https://interview-prep.coderboi.com/python/testing/pytest#q-approx-floats)
- 🟡 [How does pytest discover which tests to run?](https://interview-prep.coderboi.com/python/testing/pytest#q-test-discovery)
- 🟡 [What is an autouse fixture, and when should you use one?](https://interview-prep.coderboi.com/python/testing/pytest#q-autouse-fixtures)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/testing/pytest)

### Mocking & Patching

- 🟢 [What is mocking and why do you use it?](https://interview-prep.coderboi.com/python/testing/mocking#q-what-is-mocking)
- 🟡 [What is the difference between Mock and MagicMock?](https://interview-prep.coderboi.com/python/testing/mocking#q-mock-vs-magicmock)
- 🔴 [How does unittest.mock.patch work, and what does "patch where it's used" mean?](https://interview-prep.coderboi.com/python/testing/mocking#q-patch-where-used)
- 🟡 [What is the difference between return_value and side_effect?](https://interview-prep.coderboi.com/python/testing/mocking#q-return-value-side-effect)
- 🟡 [How do you assert a mock was called correctly?](https://interview-prep.coderboi.com/python/testing/mocking#q-call-assertions)
- 🟡 [What is autospec and why is it useful?](https://interview-prep.coderboi.com/python/testing/mocking#q-autospec)
- 🟡 [When do you use `patch.object` instead of `patch`?](https://interview-prep.coderboi.com/python/testing/mocking#q-patch-object)
- 🟡 [How do you temporarily patch a dictionary or environment variables?](https://interview-prep.coderboi.com/python/testing/mocking#q-patch-dict)
- 🟡 [What's the difference between `spec`, `spec_set`, and `autospec`?](https://interview-prep.coderboi.com/python/testing/mocking#q-mock-spec-attribute)
- 🔴 [How do you mock a property or attribute (not a method)?](https://interview-prep.coderboi.com/python/testing/mocking#q-mock-property)
- 🔴 [How do you mock an object used as a context manager?](https://interview-prep.coderboi.com/python/testing/mocking#q-mocking-context-manager)
- 🟡 [What are the downsides of over-mocking?](https://interview-prep.coderboi.com/python/testing/mocking#q-when-not-to-mock)
- 🟡 [How does `mock_open` simplify testing file I/O?](https://interview-prep.coderboi.com/python/testing/mocking#q-mock-open-helper)
- 🟢 [How do you reset a mock's recorded calls between assertions?](https://interview-prep.coderboi.com/python/testing/mocking#q-mock-reset)
- 🔴 [How do you mock an async function or coroutine?](https://interview-prep.coderboi.com/python/testing/mocking#q-async-mock)

[Full answers with code examples →](https://interview-prep.coderboi.com/python/testing/mocking)

---

## Difficulty Key

🟢 Easy — should know cold  ·  🟡 Medium — needs practice  ·  🔴 Hard — senior-level

---

## How to Use This

Use the checkboxes as a study tracker — go through each section, click the link to read the full answer, then come back and tick it off. The full answers include:

- A clear written explanation
- A working code example with inline comments
- A "Rule of thumb" line you can actually say out loud in an interview

Full site: [interview-prep.coderboi.com/python](https://interview-prep.coderboi.com/python)
