<!-- .slide: style="text-align: left;"> -->

title: Function Signature Design
<span style="font-size:.4em; margin-right:0">v1.3</span>

author: Kristoffel Pirard

url: http://github.com/xtofl/articles/monoid/monoid.md
style: night.css

<div style="font-size:.4em">
[(single-page version)](?print-pdf&pdfSeparateFragments=false)
</div>

<div style="font-size:.4em">
This slide deck is intended for use with reveal.js;
</div>
<div style="font-size:.4em">
```
articles> make function_signature_design/function_signature_design.reveal
```
</div>

---

# Function Signature Design


![pig throwing flares at itself](milewski_monoid.jpg) <!-- .element: width="300" style="display: block; margin-left: auto; margin-right: auto;" -->
<div style="font-size:.4em">credit: Bartosz Milewski</div>

--

Hidden slide

Slidedeck mainline


* CONTEXT
    * what is a function
    * single entry/exit...
        * exceptions
        * coroutines
* RATIONALE
    * why?  readability/learnability/usability
    * what is the essence the function does
    * goals of function signature
        * understand the code that uses it
        * limit documentation to the "why"
    * Abstraction levels
        * cognitive limitations (5 +- 2)
        * function length = indicator
* Our Tool Belt
    * typingontext vs. repetition
    * naming
    * contextual, implicit, domain knowledge
        * e.g. `std::lerp`, `std::iota`
    * documentation
* Types convey meaning
    * vocabulary types
    * argument type
    * argument qualifiers (sinks)
    * member function qualifiers
    * return type
    * return type qualifiers
    * Note: parameters = signature <-> arguments = call+implementation
* naming
    * explain what it does
        * to your colleague
        * to your dad
        * to your kid
    * verbs, nouns, adjectives
        * NEED INTERACTION HERE; an execise?
    * role vs. type
    * fish in the same pont
        * begin/end start/stop first/last
        * more examples?
    * context vs. repetition
    * C++: name lookup/overloading
        * asInt, asBool, asString... cast operator!
        * fromInt, fromBool, ... overloads
        * compatibility <-> onion arch. adapters
    * C++: conventional functions
        * construct/destruct
        * indexing
        * converting
        * calling (?)
    * Note: ~~foo~~ ~~bar~~
* form: 'non-functional'
    * sync/async
    * side effects
    * error handling indications



---

## Function Signature Design

Why?

Functions?

* divide and conquer
* code reuse
* composability
    * e.g. `std::sort`

--

* Readability
    * in code reviews => Quality ^^
* Learnability
    * reuse => dev speed
    * mental overhead vv
* Usability
    * useful abstraction