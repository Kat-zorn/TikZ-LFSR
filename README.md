# TikZ-LFSR

> A $\LaTeX$ package to help drawing Linear Feedback Shift Registers (LFSRs) in TikZ.

## Example

See example.tex and example.pdf for some sample source code and results.

## Commands

The package exposes the following macros:

### `\LFSR`

This command is used to draw a single LFSR.
It can optionally be given the aruments `base name` and `zero subscript`,
and it requires a binary number starting with 1.
An example is as follows. 

```LaTeX
\LFSR[%               % The `%' on the left is needed to allow multi-line to work gracefully.
  base name = s,      % The name to give to the cells of the LFSR
  zero subscript = j, % What to replace the 0-subscript by.
]{100101}             % A `1' represents a register that contributes to the final sum.
```

### `\ManyLFSR`

This command is used to draw seval parallel LFSRs whose final output is the sum of each individual output.
The syntax is the same as the `\LFSR` command, but with a list of bitstrings instead.

```LaTeX
\LFSR[%
  base name = s,      % Must be a single character. If more are given, only the first will be used.
  zero subscript = j, %
]{100101,1011}        % A comma-separated list.
```

## License

This code is licensed under CC-BY. For more information see the LICENSE.CC-BY file.

## Including the package

To use this code in a $\LaTeX$ editor, place the `.sty` file in the project directory.
Then, you can `\usepackage{tikz-lfsr}` as usual.
