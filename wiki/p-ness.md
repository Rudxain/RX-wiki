# `P`-ness
The "`p`-ness of `r`" is defined as `n / s`, where `p^n = q` (for some [don't-care](https://en.wikipedia.org/wiki/Don%27t-care_term) `q`), and `s` is the sum of all exponents in the [canonical form](https://oeis.org/wiki/Prime_factorization#Canonical_prime_factorization) of `|r|` (excluding `n`).
`r` must be rational, otherwise the p-ness is undefined.

## Examples
- the 2-ness (AKA "even-ness") of ±2 is 1, because 2=2^1 and 1/1=1
- 2-ness of ±3 is 0
- 2-ness of ±1/2 is -1
- 2-ness of ±18 is 1/3, because 18=2^1*3^2 and 1/(2+1)=1/3
- 2-ness of ±4/3 is 1, because 4/3=2^2*3^-1 and 2/(|-1|+1)=1
- 3-ness of ±192 is 1/7, because 192 = 2^6 * 3^1 and 1/(6+1)=1/7
