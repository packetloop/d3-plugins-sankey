d3-sankey
=========

A fork of D3js's Sankey plugin

Demo: <http://bost.ocks.org/mike/sankey/>

```js
var sankey = d3.sankey()
    .size([width, height])
    .nodeWidth(15)
    .nodePadding(10)
    .nodes(energy.nodes)
    .links(energy.links)
    .layout(32);
```

```
var path = sankey.link();
```

## Additional Features

The `d3.sankey()` closure supports an additional `options` hash not
found in the standard implementation.

It allows the following additional features.

* `customSort : (defaultSort) => (a:node, b:node) => :int`

A custom sort function to determine node order. The option value should 
be a factory for a compare function. The existing compare function is
given to the factory and your custom compare function should be
returned.