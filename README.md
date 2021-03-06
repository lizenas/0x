# Ox
Converts between hex, binary, octal, and decimal. Requires bash 4.0+

Usage: Ox [options] \<value\>

Options:
```
-h  --help     Display help message and exit
-q  --quiet    Diables printing of input value, removes type prefix from converted types
-D  --dec      Disable printing of decimal value
-H  --no-hex   Disable printing of hexadecimal value
-B  --no-bin   Disable printing of binary value
-O  --no-oct   Disable printing of octal value
```
Valid values:

- Hex values start with 0x, case insensitive (E.g. 0xED, 0xed)
- Binary values start with 0b (E.g. 0b1010, 0B1010)
- Octal values start with 0 (E.g. 0555, 0777)
- Decimal values are positive integers that do not fit the above parameters (E.g. 76, 52)

Examples:

```Ox 0b1110``` outputs:
```
Input:   0b110
Decimal: 6
Hex:     0x6
Octal:   006
```

```Ox 0xAE6 0xeee``` outputs:
```
Input:   0xAE6
Decimal: 2790
Binary:  0b101011100110
Octal:   05346

Input:   0xeee
Decimal: 3822
Binary:  0b111011101110
Octal:   07356
```

```Ox 0775 36``` outputs:
```
Input:   0777
Decimal: 511
Hex:     0x1FF
Binary:  0b111111111

Input:   36
Hex:     0x36
Binary:  0b110110
Octal:   066
```
