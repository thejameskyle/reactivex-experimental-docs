You can use the `generate` operator to create simple Observables that can
generate their next emissions, and can determine when to terminate, based on the
value of the previous emission. The basic form of `generate` takes four
parameters:

1. The first item to emit.
1. A function to test an item to determine whether to emit it (true) or
  terminate the Observable (`false`).
1. A function to generate the next item to test and emit based on the value of
  the previous item.
1. A function to transform items before emitting them.

You can also pass in as an optional fifth parameter a [Scheduler]() that
`generate` will use to create and emit its sequence (it uses `currentThread`
by default).
