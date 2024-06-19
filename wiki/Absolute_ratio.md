# Absolute ratio
Defined as the [quotient](https://en.wikipedia.org/wiki/Quotient) between the maximum and minimum [absolute-values](https://en.wikipedia.org/wiki/Absolute_value) of both input arguments.

## Applications
It can be used to guarantee that integer division is always greater than 0, which "preserves" the information of the operands.

## Implementation
[PFP](https://en.wikipedia.org/wiki/Pure_functional_programming)-style code in both Python and TypeScript, respectively:
```py
from typing import Final, Callable
# there's `TypeVar` but `//` forces us to `def` 2 APIs

fabs_ratio: Final[Callable[[float, float], float]] = lambda x, y, /: (
	lambda x, y: max(x, y) / min(x, y)
)(abs(x), abs(y))

iabs_ratio: Final[Callable[[int, int], int]] = lambda x, y, /: (
	lambda x, y: max(x, y) // min(x, y)
)(abs(x), abs(y))
```
```ts
type numeric = number | bigint

const
	max = <T extends numeric,>(x: T, y: T) =>
		x < y ? y : x,
	min = <T extends numeric,>(x: T, y: T) =>
		x > y ? y : x,
	abs = <T extends numeric,>(x: T) =>
		x < 0 ? -x as T : x

const abs_ratio = <T extends numeric,>(x: T, y: T) =>
	(max(abs(x), abs(y)) / min(abs(x), abs(y))) as T

// as of TS v5, those type-asserts are necessary:
// https://github.com/microsoft/TypeScript/issues/49558#issuecomment-2177373544
```

## See also
[Rust `lib`](https://github.com/Rudxain/abs_ratio/blob/main/src/lib.rs)
