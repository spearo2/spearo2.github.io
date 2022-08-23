---
layout: post
category: theory
---

# Combinational Logic

This is basically applications of past 3 chapters.

Combinational Logic is boolean expression that has combinational logical circuit.

Input --> Combinational Circuit --> Output

Here, we assume that there is no memory element, no feedback from the outputs to the inputs.

Outputs of at any time are uniquely determined from the present combinations of inputs.

Ex) <img src="{{site.url}}/assets/images/theory/ld_circuit1.png" width="auto" height="auto" alt="circuit1">

## Methods to convert truth tables (TT) to boolean equations.

1. Collect combinations of inputs that make the ouput = 1
  -->Each vatiable is bound with AND. Each term is bound with OR.
2. Collect combinations of inputs that make the ouput = 0
  -->Each vatiable is bound with OR. Each term is bound with AND.

Let's say there is a TT as follows:

x      | y     | z    |Y
------ | ------|------|------
0       |  0     | 0     | 0
0       |  0     | 1     | 0
0       |  1     | 0     | 0
0       |  1     | 1     | 1
1       |  0     | 0     | 1
1       |  0     | 1     | 1
1       |  1     | 0     | 1
1       |  1     | 1     | 1

### Following Method 1.

Y = x'yz + xy'z + xyz' + xyz

### Following Method 2.

Y = (x+y+z)(x+y+z')(x+y'+z)