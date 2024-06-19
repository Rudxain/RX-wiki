# Absolute ratio
[PFP](https://en.wikipedia.org/wiki/Pure_functional_programming)-style algorithms in both Python and TypeScript, respectively:
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
```

## See also
[Rust `lib`](https://github.com/Rudxain/abs_ratio/blob/main/src/lib.rs)
