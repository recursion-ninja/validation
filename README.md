# Validation

![CSIRO's Data61 Logo](https://raw.githubusercontent.com/qfpl/assets/master/data61-transparent-bg.png)

Several data-types like Either but with differing properties and type-class
instances.

Library support is provided for those different representations, include
`lens`-related functions for converting between each and abstracting over their
similarities.

Download from [hackage](http://hackage.haskell.org/package/validation).

* `Validation`

  The `Validation` data type is isomorphic to `Either`, but has an instance
  of `Applicative` that accumulates on the error side. That is to say, if two
  (or more) errors are encountered, they are appended using a `Semigroup`
  operation.

  As a consequence of this `Applicative` instance, there is no corresponding
  `Bind` or `Monad` instance. `Validation` is an example of, "An applicative
  functor that is not a monad."

