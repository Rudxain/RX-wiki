# Base-Coded Radix
BCR is a family of radix-to-numeral encodings (such as [BTTs](https://en.wikipedia.org/wiki/Binary-to-text_encoding)) for positional numeral systems. The most well-known members being [BCD](https://en.wikipedia.org/wiki/Binary-coded_decimal) (for radix `|| * |||||` AKA "ten") and [BCT](https://en.wikipedia.org/wiki/Ternary_numeral_system#Binary-coded_ternary) (for radix `|||` AKA "three").

These encodings make it possible to efficiently operate on radix `N` data and numeric values, while sacrificing "minimal" memory (especially the "packed" variants).
