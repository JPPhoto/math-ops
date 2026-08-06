# math_ops

Custom InvokeAI nodes for basic numeric operations and type conversion.

## Nodes

### Min/Max/Average

Accepts two numeric values and returns:

* The smaller value
* The larger value
* The arithmetic mean

#### Inputs

| Input |  Type | Default | Description  |
| ----- | ----: | ------: | ------------ |
| `x`   | Float |   `0.0` | First value  |
| `y`   | Float |   `0.0` | Second value |

#### Outputs

| Output |  Type | Description                   |
| ------ | ----: | ----------------------------- |
| `min`  | Float | Smaller input value           |
| `max`  | Float | Larger input value            |
| `avg`  | Float | Arithmetic mean of the inputs |

Example:

```text
x = 4
y = 10

min = 4
max = 10
avg = 7
```

### Integer to Float Conversion

Converts an integer value to a floating-point value.

#### Input

| Input   |    Type | Description        |
| ------- | ------: | ------------------ |
| `value` | Integer | Integer to convert |

#### Output

| Output  |  Type | Description                    |
| ------- | ----: | ------------------------------ |
| `value` | Float | Converted floating-point value |

Example:

```text
Input:  5
Output: 5.0
```

### Float to Integer Conversion

Converts a floating-point value to an integer using Python's `int()` conversion.

The fractional portion is discarded toward zero.

#### Input

| Input   |  Type | Description                     |
| ------- | ----: | ------------------------------- |
| `value` | Float | Floating-point value to convert |

#### Output

| Output  |    Type | Description             |
| ------- | ------: | ----------------------- |
| `value` | Integer | Converted integer value |

Examples:

```text
Input:  5.9
Output: 5

Input:  -5.9
Output: -5
```

## Installation

Clone the repository into the directory used by your InvokeAI installation for custom nodes:

```bash
git clone git@github.com:JPPhoto/math_ops.git
```

Restart InvokeAI after installation so the nodes are discovered and registered.

## Files

```text
math_ops/
|-- __init__.py
|-- math_ops.py
|-- LICENSE
`-- README.md
```

## Requirements

* InvokeAI
* Python 3

The node imports use InvokeAI's invocation API and primitive numeric output types.

## License

See the `LICENSE` file for licensing information.
