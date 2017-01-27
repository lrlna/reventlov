# reventlov

Genetically evolve your cellular automata one cell at a time.

This is a partner package to [olivaw](github.com/lrlna/olivaw)

# Usage

```js
var reventlov = require('reventlov')

var automaton = reventlov({
  rule: 110,
  population: 101,
  life: 500,
  generation: 20
})

// returns an end rule, or the rule that was completed by the end
var evolution = automaton.evolve()
```

## automaton = reventlov(opts)
Create a new instance of reventlov by providing options. All four options are
required:
- __opts.rule__: one of 256 rules for the automata to follow 
- __opts.population__: the population size, or the number of cells you want to
work with 
- __opts.life__: life span of an automata instance, or the number of years it
will run for 
- __opts.generation__: the number of generations you want to evolve your automata
for. Usually, more 'time' for evolution yields better results. 

## reventlov.evolve()
Runs through the specified number of generations and evolves automata as it goes.
Returns the last rule that reventlov achieved at the end of the specified number
of generations.

## Install
```
npm install reventlov
```
